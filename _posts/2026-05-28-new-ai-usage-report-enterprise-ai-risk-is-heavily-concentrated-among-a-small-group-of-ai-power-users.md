---
title: 'New AI Usage Report: Enterprise AI Risk Is Heavily Concentrated Among a Small Group of AI "Power users"'
date: 2026-05-28
permalink: /posts/2026/05/28/new-ai-usage-report-enterprise-ai-risk-is-heavily-concentrated-among-a-small-group-of-ai-power-users/
tags:
- veille-cyber
- hackernews
---
### État des lieux de l'usage de l'IA en entreprise : risques et gouvernance

Le rapport "State of AI Usage 2026" de LayerX Security révèle que les risques liés à l'IA en entreprise ne sont pas uniformes, mais concentrés au sein d'un petit groupe d'utilisateurs intensifs ("Power users") et via une multitude d'outils échappant aux contrôles traditionnels.

**Points clés :**
*   **Concentration des risques :** 5 % des utilisateurs génèrent une part disproportionnée des interactions et des volumes de données, exposant davantage l'organisation.
*   **Fragmentation des outils :** L'usage s'étend au-delà des chatbots vers des extensions de navigateur, des connecteurs SaaS et des assistants intégrés, rendant la visibilité difficile pour les équipes sécurité.
*   **Identités personnelles vs professionnelles :** Près de 50 % des conversations ont lieu via des comptes personnels, échappant aux politiques de rétention et de conformité de l'entreprise.
*   **Exposition des données :** Plus de 6 % des conversations contiennent des données sensibles (principalement des informations personnelles, financières ou informatiques). DeepSeek et ChatGPT présentent les taux d'exposition les plus élevés, contrairement à Copilot M365.

**Vulnérabilités identifiées :**
*   **Extensions de navigateur :** 15 % des employés utilisent des extensions IA, dont 75 % nécessitent des permissions critiques. Plus de 16 % de ces extensions présentent des vulnérabilités connues (CVE non spécifiées dans le rapport, mais l'article souligne un risque intrinsèque lié à la surface d'attaque des permissions).
*   **Connecteurs IA :** Les accès programmatiques (GitHub, Slack, SharePoint) permettent aux systèmes d'IA de puiser directement dans les bases de connaissances internes, augmentant la surface d'exposition en cas de compromission.

**Recommandations pour les CISO :**
*   **Ciblage :** Prioriser la surveillance et la sécurisation des "Power users" plutôt que de tenter de contrôler indistinctement tous les employés.
*   **Gouvernance :** Bannir l'usage de comptes personnels pour les activités professionnelles afin de garantir la visibilité sur les flux de données.
*   **Protection dynamique :** Mettre en place des garde-fous "inline" (en temps réel) capables d'analyser les prompts et les transferts de fichiers plutôt qu'une simple politique binaire de blocage.
*   **Élargissement du périmètre :** Intégrer les extensions de navigateur et les outils SaaS intégrés dans la stratégie de gestion du Shadow AI.

---
[Source](https://thehackernews.com/2026/05/new-ai-usage-report-enterprise-ai-risk.html){:target="_blank"}
