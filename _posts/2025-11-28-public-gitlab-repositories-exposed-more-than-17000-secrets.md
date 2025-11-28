---
title: 'Public GitLab repositories exposed more than 17,000 secrets'
date: 2025-11-28
permalink: /posts/2025/11/28/public-gitlab-repositories-exposed-more-than-17000-secrets/
tags:
- veille-cyber
- bleepingcomp
---
**Des milliers de secrets exposés dans les dépôts GitLab publics**

Une analyse approfondie de 5,6 millions de dépôts publics sur GitLab Cloud a révélé plus de 17 000 secrets, tels que des clés API, des mots de passe et des jetons, exposés dans plus de 2 800 domaines uniques. L'outil open-source TruffleHog a été utilisé pour cette découverte, qui a permis d'identifier près de trois fois plus de secrets que lors d'une analyse similaire sur Bitbucket. Les secrets les plus fréquemment trouvés concernent Google Cloud Platform, MongoDB, Telegram et OpenAI.

**Points Clés :**

*   Plus de 17 000 secrets exposés dans 5,6 millions de dépôts GitLab publics.
*   Ces secrets proviennent de plus de 2 800 domaines distincts.
*   La majorité des secrets concernent des plateformes cloud et des services d'authentification.
*   Des actions de notification et de révocation de secrets ont été entreprises par les organisations concernées, mais certains restent exposés.

**Vulnérabilités :**

*   L'exposition de secrets dans des dépôts publics constitue une faille de sécurité majeure, permettant un accès non autorisé à des ressources et des données sensibles.
*   Bien que des CVE spécifiques ne soient pas mentionnés pour chaque secret individuel, cette pratique de stockage de secrets en clair dans le code source est intrinsèquement vulnérable.

**Recommandations :**

*   Mettre en place des politiques strictes interdisant le stockage de secrets directement dans le code source.
*   Utiliser des solutions de gestion des secrets (secrets management) pour stocker et distribuer de manière sécurisée les informations sensibles.
*   Effectuer des scans réguliers des dépôts de code pour détecter et supprimer les secrets exposés.
*   Mettre en œuvre des mécanismes d'authentification et d'autorisation robustes pour limiter l'accès aux ressources critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/public-gitlab-repositories-exposed-more-than-17-000-secrets/){:target="_blank"}
