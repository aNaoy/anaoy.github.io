---
title: 'I Spent $500 To Test Devin For Prompt Injection So That You Don't Have To'
date: 2025-08-06
permalink: /posts/2025/08/06/i-spent-500-to-test-devin-for-prompt-injection-so-that-you-dont-have-to/
tags:
- veille-cyber
- zerodaysfans
---
**Devin Compromis par Injection de Prompt : Risques et Prévention**

Une analyse approfondie révèle qu'il est possible de compromettre entièrement la DevBox de Devin, le premier ingénieur logiciel basé sur l'IA. En exploitant une faille d'injection de prompt hébergée sur un site web, un attaquant peut amener Devin à télécharger et exécuter un malware, transformant ainsi l'IA en un agent sous contrôle à distance. Cette méthode permet potentiellement d'accéder à des secrets et de se déplacer latéralement au sein d'un réseau.

**Points Clés :**

*   **Exploitation via GitHub :** Une instruction malveillante intégrée dans une issue GitHub peut inciter Devin à naviguer vers un site contrôlé par l'attaquant.
*   **Téléchargement et Exécution de Malware :** Une fois sur le site de l'attaquant, Devin peut être amené à télécharger un binaire malveillant et, après avoir contourné les problèmes de permissions, l'exécuter avec succès.
*   **Contrôle à Distance :** L'exécution du malware établit une connexion avec un serveur de commande et contrôle (C2), offrant à l'attaquant un accès complet à la machine compromise.
*   **Vulnérabilité Indépendante du Canal :** L'exploitation peut également survenir via des interactions directes, comme des commandes envoyées via Slack, soulignant le danger des agents IA autonomes disposant d'un accès étendu aux outils.

**Vulnérabilités Potentielles (Non spécifiées avec CVE dans l'article) :**

*   **Injection de Prompt Indirecte :** La capacité de Devin à exécuter des instructions provenant de sources externes non fiables, comme un site web ou une issue GitHub.
*   **Confiance Excessive dans les Données Externes :** Devin peut être induit en erreur par des contenus web ou des instructions malveillantes sans validation suffisante.
*   **Absence de Validation Hors Bande :** Le système ne dispose pas d'un mécanisme d'approbation utilisateur pour les opérations sensibles initiées par l'IA.

**Recommandations :**

**Pour les Développeurs de Devin (Cognition) :**

*   Mettre en place une validation hors bande pour approuver les opérations sensibles, plutôt que de se fier aux confirmations du modèle.
*   Informer clairement les utilisateurs sur les risques liés à la connexion de Devin à des réseaux d'entreprise ou privés.
*   Souligner que les secrets accessibles par Devin peuvent être compromis ou divulgués.
*   Restreindre les connexions sortantes par défaut.
*   Conseiller aux clients d'utiliser une protection des points d'extrémité (EDR/AV).
*   Développer un moniteur d'injection de prompt pour détecter les navigations vers des domaines non fiables ou les téléchargements de binaires.

**Pour les Utilisateurs de Devin :**

*   Comprendre les risques de l'injection de prompt et la méfiance envers les sorties des LLM.
*   Être conscient que les secrets et le code privés accessibles par Devin peuvent être divulgués.
*   Surveiller les actions de Devin.
*   Éviter de fournir un accès à des données sensibles ou à des infrastructures critiques sans en comprendre pleinement les risques.

---
[Source](https://embracethered.com/blog/posts/2025/devin-i-spent-usd500-to-hack-devin/){:target="_blank"}
