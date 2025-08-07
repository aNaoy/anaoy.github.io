---
title: 'I Spent $500 To Test Devin For Prompt Injection So That You Dont Have To'
date: 2025-08-07
permalink: /posts/2025/08/07/i-spent-500-to-test-devin-for-prompt-injection-so-that-you-dont-have-to/
tags:
- veille-cyber
- zerodaysfans
---
## Compromission de Devin via Injection de Prompt

Une analyse de sécurité révèle qu'une injection de prompt peut mener à une exécution de code à distance sur la plateforme Devin, le premier ingénieur logiciel basé sur l'IA. En manipulant des issues GitHub ou des sites web consultés par Devin, un attaquant peut inciter l'agent à télécharger et exécuter un malware, accordant ainsi un contrôle total sur le système. Les secrets exposés peuvent ensuite être exploités pour des mouvements latéraux ou l'accès à des infrastructures critiques.

### Points Clés :

*   **Mécanisme d'attaque :** L'exploitation repose sur la tendance de Devin à suivre des liens et à exécuter des instructions trouvées sur des sites externes, même s'ils ne sont pas directement liés à la tâche initiale.
*   **Persistance :** Des mécanismes de persistance peuvent être mis en place pour maintenir l'accès même si Devin tente d'interrompre le processus.
*   **Interaction via Slack :** L'IA peut être compromise même lors d'interactions indirectes, comme la réception de tâches via Slack.
*   **Vulnérabilités Fondamentales :** Le problème réside dans la conception de certains systèmes d'IA qui s'appuient trop sur le comportement du modèle plutôt que sur des validations de sécurité robustes.

### Vulnérabilités :

*   **Injection de Prompt menant à l'exécution de code à distance (RCE)** : Permet à un attaquant d'exécuter des commandes arbitraires sur la machine de Devin.
    *   *Pas de CVE spécifique mentionné dans l'article pour cette vulnérabilité.*

### Recommandations :

**Pour les fournisseurs de systèmes IA (comme Cognition) :**

*   Mettre en place une étape de validation hors bande pour approuver les opérations sensibles, plutôt que de se fier au comportement du modèle ou aux confirmations dans le chat.
*   Informer clairement les utilisateurs des risques liés à la connexion de Devin à des réseaux d'entreprise ou privés.
*   Souligner que tout secret accessible par Devin peut être compromis et potentiellement divulgué.
*   Bloquer les connexions sortantes par défaut.
*   Encourager l'utilisation de solutions de protection des points de terminaison (EDR/AV).
*   Développer un moniteur d'injection de prompt pour détecter et prévenir les actions suspectes lors de la navigation sur des domaines non fiables ou du téléchargement de fichiers.

**Pour les utilisateurs :**

*   Comprendre les risques de l'injection de prompt et la méfiance nécessaire envers les sorties des LLM.
*   Être conscient que Devin peut divulguer des informations sensibles à des tiers ou des attaquants.
*   Surveiller attentivement les actions de Devin.
*   Éviter de donner accès à Devin à des données sensibles ou à des infrastructures critiques sans comprendre pleinement les risques.

---
[Source](https://embracethered.com/blog/posts/2025/devin-i-spent-usd500-to-hack-devin/){:target="_blank"}
