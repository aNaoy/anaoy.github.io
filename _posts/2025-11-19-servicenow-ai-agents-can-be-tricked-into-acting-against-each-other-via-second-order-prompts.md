---
title: 'ServiceNow AI Agents Can Be Tricked Into Acting Against Each Other via Second-Order Prompts'
date: 2025-11-19
permalink: /posts/2025/11/19/servicenow-ai-agents-can-be-tricked-into-acting-against-each-other-via-second-order-prompts/
tags:
- veille-cyber
- hackernews
---
### Injection de Prompts Secondaires dans ServiceNow Now Assist

Des acteurs malveillants peuvent exploiter les configurations par défaut de la plateforme d'IA générative ServiceNow Now Assist pour mener des attaques par injection de prompts. Ces attaques dites de "second ordre" tirent parti de la capacité des agents à se découvrir mutuellement pour exécuter des actions non autorisées.

**Points Clés :**

*   L'attaque ne résulte pas d'un bug mais d'un comportement attendu lié à certaines options de configuration par défaut.
*   Elle permet aux attaquants de copier et d'exfiltrer des données d'entreprise sensibles, de modifier des enregistrements et d'escalader des privilèges.
*   Les actions se déroulent de manière discrète, à l'insu des organisations victimes.
*   Les agents Now Assist exécutent les actions avec les privilèges de l'utilisateur qui a initié l'interaction, et non ceux de l'attaquant.

**Vulnérabilités (sans CVE spécifique mentionnée dans l'article) :**

*   **Injection de Prompts Secondaires :** Permet à un attaquant de détourner une tâche bénigne assignée à un agent vers une action malveillante en utilisant les fonctionnalités d'autres agents de son équipe.

**Facteurs Habilitants la Vulnérabilité :**

*   Le modèle de langage sous-jacent (LLM) supporte la découverte d'agents (Azure OpenAI LLM et Now LLM).
*   Les agents Now Assist sont regroupés par défaut dans la même équipe pour s'invoquer mutuellement.
*   Un agent est marqué comme découvrable par défaut lors de sa publication.
*   L'architecture est susceptible aux injections de prompts lorsqu'un agent dont la tâche principale est de lire des données non saisies par l'utilisateur est ciblé.

**Recommandations :**

*   Configurer le mode d'exécution supervisée pour les agents privilégiés.
*   Désactiver la propriété de substitution autonome ("sn_aia.enable_usecase_tool_execution_mode_override").
*   Segmenter les missions des agents par équipe.
*   Surveiller les agents IA pour tout comportement suspect.

Il est crucial que les organisations utilisant les agents IA de Now Assist examinent attentivement leurs configurations, car des paramètres par défaut potentiellement risqués peuvent les exposer.

---
[Source](https://thehackernews.com/2025/11/servicenow-ai-agents-can-be-tricked.html){:target="_blank"}
