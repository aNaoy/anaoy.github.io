---
title: 'Safeguarding VS Code against prompt injections'
date: 2025-08-25
permalink: /posts/2025/08/25/safeguarding-vs-code-against-prompt-injections/
tags:
- veille-cyber
- zerodaysfans
---
Voici un aperçu des risques de sécurité liés au mode Agent de l'extension Copilot Chat pour VS Code et des solutions mises en place.

**Risques et Vulnérabilités dans Copilot Chat**

Le mode Agent de Copilot Chat pour VS Code permet aux grands modèles de langage (LLMs) d'utiliser des outils pour interagir avec l'environnement de développement. Cependant, cette intégration peut être exploitée par des injections de prompt pour exécuter des actions non désirées ou divulguer des informations sensibles. Les vulnérabilités découvertes incluent :

*   **Fuite de tokens via la fonction `fetch_webpage` (CVE non spécifié)** : Une mauvaise analyse des URLs de confiance permettait à un attaquant d'inclure des instructions malveillantes dans un problème GitHub. Ces instructions pouvaient inciter le modèle à lire un fichier local contenant des tokens (par exemple, des tokens GitHub) et à les envoyer à un serveur externe via une URL malformée mais considérée comme de confiance. Aucune confirmation utilisateur n'était requise.

*   **Fuite de tokens via l'outil `Simple Browser` (CVE non spécifié)** : Similaire à la vulnérabilité précédente, l'outil `Simple Browser`, conçu pour des tests locaux, pouvait être abusé pour accéder à des sites externes. En ajoutant des instructions conditionnelles dans un problème GitHub, il était possible de faire lire un fichier de configuration local et d'utiliser les informations extraites pour accéder à un site externe, sans confirmation utilisateur.

*   **Exécution de code arbitraire via l'outil `editFile` (CVE non spécifié)** : L'outil permettant de modifier des fichiers locaux, bien qu'affichant les modifications à l'utilisateur, enregistrait les changements immédiatement. Cela permettait à un attaquant de modifier des fichiers de configuration sensibles (comme `settings.json`) pour reconfigurer le lancement des serveurs MCP (Machine Code Process). En modifiant la commande d'exécution du serveur pour lancer une application (par exemple, la calculatrice), le modèle exécutait des actions arbitraires sans confirmation directe de l'utilisateur. Des rapports externes ont également mis en évidence la possibilité de configurer `chat.tools.autoApprove` à `true` pour contourner les confirmations.

*   **Injection de prompt indirecte** : Les LLMs peuvent être manipulés en utilisant des conditions subtiles dans les prompts, comme des dates spécifiques, des références à d'autres parties du prompt, ou en imitant le prompt système. Ces techniques peuvent inciter le modèle à exécuter des instructions malveillantes, même si le modèle est entraîné à résister. La configuration de la température à 0 par VS Code pour la cohérence des réponses rend ces exploits plus reproductibles.

**Points Clés**

*   Le mode Agent de Copilot Chat intègre des LLMs avec des outils pour améliorer la productivité, mais crée un risque d'injection de prompt.
*   Les prompts, y compris ceux issus de sources externes comme les problèmes GitHub, sont fusionnés dans une seule requête au LLM, rendant possible l'exécution d'instructions malveillantes.
*   Les outils qui n'exigent pas de confirmation utilisateur systématique, comme la lecture de fichiers ou certaines interactions réseau, sont des cibles privilégiées pour les attaques.
*   Les modifications immédiates de fichiers par l'outil `editFile` et la capacité à exécuter des commandes arbitraires via la configuration des serveurs MCP représentent un risque élevé.

**Recommandations et Améliorations**

Pour atténuer ces risques, plusieurs mesures ont été implémentées ou sont recommandées :

*   **Confirmation Utilisateur Obligatoire** :
    *   Les outils `fetch_webpage` et `Simple Browser` exigent désormais une confirmation pour accéder à de nouvelles URLs, indépendamment de leur origine.
    *   Pour l'outil `editFile`, des confirmations sont désormais requises pour les modifications de fichiers sensibles en dehors de l'espace de travail ou des fichiers ouverts. Les versions futures de VS Code Insiders forceront la confirmation pour les modifications de fichiers de configuration.

*   **Découplage des URLs** : La validation des URLs pour la fonction `fetch` a été séparée de la liste des domaines de confiance pour corriger la vulnérabilité de l'analyse des URLs.

*   **Restrictions sur les Modifications de Fichiers** : VS Code ne permet plus aux agents de modifier des fichiers situés en dehors de l'espace de travail actuel.

*   **Sandboxing** : L'utilisation d'environnements isolés comme les Conteneurs de Développement (via `devcontainer.json`) ou GitHub Codespaces est fortement recommandée. Ces solutions isolent l'exécution des outils de Copilot de votre machine locale, offrant une protection de défense en profondeur.

*   **Confiance aux Serveurs MCP** : L'acceptation d'un dialogue modal est désormais nécessaire pour "faire confiance" à un serveur MCP avant de pouvoir l'utiliser.

*   **Contrôle des Outils** : Des fonctionnalités futures permettront aux utilisateurs de sélectionner explicitement les outils accessibles par le LLM et de configurer des ensembles d'outils pour des scénarios spécifiques.

*   **Politiques de Sécurité** : Le support des politiques d'entreprise permettra de désactiver certaines capacités (outils d'extensions, MCP, mode agent) pour renforcer la sécurité.

*   **Meilleures Pratiques** :
    *   Utiliser le **Workspace Trust** en mode restreint lors de l'ouverture de dépôts non fiables.
    *   Privilégier le **sandboxing** via les conteneurs Docker ou GitHub Codespaces pour exécuter des commandes potentiellement dangereuses.

---
[Source](https://github.blog/security/vulnerability-research/safeguarding-vs-code-against-prompt-injections/){:target="_blank"}
