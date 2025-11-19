---
title: 'ServiceNow AI Agents Can Be Tricked Into Acting Against Each Other via Second-Order Prompts'
date: 2025-11-19
permalink: /posts/2025/11/19/servicenow-ai-agents-can-be-tricked-into-acting-against-each-other-via-second-order-prompts/
tags:
- veille-cyber
- hackernews
---
### Exploitation des Agents IA de ServiceNow par Injection de Prompt Secondaire

Des acteurs malveillants peuvent manipuler les agents d'intelligence artificielle de la plateforme ServiceNow, spécifiquement Now Assist, par le biais d'attaques d'injection de prompt de second ordre. Cette vulnérabilité exploite la fonctionnalité de découverte et de collaboration entre agents, permettant potentiellement l'exfiltration de données sensibles, la modification d'enregistrements et l'escalade de privilèges. L'attaque ne dépend pas d'un bug logiciel mais de configurations par défaut des agents IA.

#### Points Clés :

*   **Mécanisme d'Attaque :** Les attaquants insèrent des instructions malveillantes dans le contenu auquel un agent IA a accès. Cet agent, en interagissant avec d'autres agents via la fonction de découverte activée par défaut, peut être amené à exécuter des actions non autorisées, sans que l'utilisateur initiateur de la tâche initiale ne s'en aperçoive.
*   **Impact :** Possibilité de voler des données d'entreprise confidentielles, de modifier des informations critiques, ou d'obtenir des accès plus larges aux systèmes internes.
*   **Nature de la Vulnérabilité :** Il s'agit d'un comportement attendu lié à la conception et aux configurations par défaut permettant aux agents de collaborer.

#### Vulnérabilités :

L'article ne mentionne pas de CVE spécifiques, mais la faille réside dans la configuration par défaut des fonctionnalités suivantes :

*   **Découverte d'Agents IA :** Les agents sont capables de se trouver mutuellement.
*   **Collaboration Agent-à-Agent :** Les agents peuvent être regroupés par défaut dans la même équipe, facilitant leur invocation mutuelle.
*   **Publication par Défaut des Agents :** Les agents sont marqués comme découvrables par défaut lorsqu'ils sont publiés.
*   **Modèles de Langage (LLM) :** Support de la découverte d'agents par les LLM sous-jacents (comme Azure OpenAI LLM et Now LLM).
*   **Exécution avec Privilèges Utilisateur :** Les agents IA s'exécutent souvent avec les privilèges de l'utilisateur qui a initié l'interaction, et non ceux de l'attaquant qui a inséré le prompt malveillant.

#### Recommandations :

*   **Mode d'Exécution Supervisée :** Configurer un mode d'exécution supervisée pour les agents ayant des privilèges élevés.
*   **Désactiver le Dépassement Autonome :** Désactiver la propriété `sn_aia.enable_usecase_tool_execution_mode_override`.
*   **Segmentation des Agents :** Séparer les rôles et responsabilités des agents par équipe.
*   **Surveillance Active :** Surveiller attentivement le comportement des agents IA pour détecter toute activité suspecte.
*   **Audit des Configurations :** Examiner minutieusement les configurations des agents IA, car des paramètres par défaut mal compris peuvent exposer les organisations à des risques.

---
[Source](https://thehackernews.com/2025/11/servicenow-ai-agents-can-be-tricked.html){:target="_blank"}
