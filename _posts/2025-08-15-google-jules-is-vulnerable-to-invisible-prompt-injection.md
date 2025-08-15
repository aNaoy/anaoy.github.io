---
title: 'Google Jules is Vulnerable To Invisible Prompt Injection'
date: 2025-08-15
permalink: /posts/2025/08/15/google-jules-is-vulnerable-to-invisible-prompt-injection/
tags:
- veille-cyber
- zerodaysfans
---
### Injection Invisible dans Jules : Manipulation via des Caractères Unicode Cachés

Les modèles Gemini de Google, et par extension des applications comme Google Jules, sont affectés par une vulnérabilité permettant des injections de prompts invisibles. Cette faille exploite des caractères Unicode spécifiques, invisibles dans l'interface utilisateur, que les modèles interprètent comme des instructions. Cela ouvre la voie à l'exécution de commandes arbitraires, l'ajout de code malveillant, et potentiellement à une compromission du système. La vulnérabilité, signalée à Google il y a plus d'un an, n'a pas été corrigée au niveau du modèle ou de l'API.

**Points clés :**

*   Les modèles Gemini interprètent certains caractères Unicode Tag comme des instructions exécutables.
*   Ces caractères sont invisibles dans les interfaces, rendant les attaques difficiles à détecter.
*   Jules, une application utilisant Gemini, peut être manipulé pour ajouter du code malveillant ou exécuter des commandes via des issues GitHub infectées.
*   La fonctionnalité de "tagging" de Jules sur GitHub simplifie le ciblage, car l'agent copie directement le contenu de l'issue, y compris les caractères cachés.

**Vulnérabilités :**

*   **Injection de Prompt Invisible par Caractères Unicode Tag :** Les modèles Gemini sont sensibles aux caractères Unicode Tag qui sont interprétés comme des instructions directes. Bien qu'aucun numéro CVE spécifique ne soit mentionné pour cette classe de vulnérabilité au niveau du modèle, cela s'inscrit dans la catégorie plus large des vulnérabilités d'injection de prompt dans les grands modèles de langage.

**Recommandations :**

*   **Gestion Prudente des Codes et Secrets :** Éviter de confier à Jules des codes sources sensibles, des secrets, ou tout ce qui pourrait faciliter un mouvement latéral dans un système.
*   **Prudence avec les Sources Non Fiables :** Ne pas assigner à Jules des issues GitHub ou des données d'entrée provenant de sources non vérifiées. Les instructions malveillantes peuvent être dissimulées dans le texte.
*   **Examen Rigoureux des Plans Proposés :** Examiner attentivement les plans générés par Jules pour identifier d'éventuelles avenues d'attaque ou des comportements inattendus.
*   **Vérification du Code Généré par IA :** Toujours relire méticuleusement le code produit par des intelligences artificielles avant de l'intégrer pour détecter erreurs et portes dérobées.

---
[Source](https://embracethered.com/blog/posts/2025/google-jules-invisible-prompt-injection/){:target="_blank"}
