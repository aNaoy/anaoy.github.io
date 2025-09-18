---
title: 'ShinyHunters claims 1.5 billion Salesforce records stolen in Drift hacks'
date: 2025-09-18
permalink: /posts/2025/09/18/shinyhunters-claims-15-billion-salesforce-records-stolen-in-drift-hacks/
tags:
- veille-cyber
- bleepingcomp
---
### Acteurs de Menace Volent 1.5 Milliard d'Enregistrements Salesforce

Un groupe d'extorsion, se faisant appeler "Scattered Lapsus$ Hunters" (anciennement ShinyHunters, Scattered Spider, Lapsus$), revendique le vol de plus de 1.5 milliard d'enregistrements de données provenant de 760 entreprises via des jetons OAuth Salesloft Drift compromis. Ces jetons ont été découverts après une intrusion dans le dépôt GitHub de Salesloft, permettant l'accès à des secrets, notamment ces jetons.

Ces jetons ont été utilisés pour accéder à des tables Salesforce importantes telles que "Account", "Contact", "Case", "Opportunity" et "User", dérobant un volume considérable de données, dont des informations sensibles contenues dans les tickets de support client. Les acteurs ont ensuite exploité des secrets trouvés dans les données volées, tels que des identifiants et des clés d'accès AWS et Snowflake, pour tenter de compromettre d'autres environnements.

Parmi les nombreuses entreprises touchées figurent Google, Cloudflare, Zscaler, Tenable, CyberArk, Elastic, BeyondTrust, Proofpoint, JFrog, Nutanix, Qualys, Rubrik, Cato Networks et Palo Alto Networks. Le FBI a émis un avertissement concernant ces activités. Bien que les attaquants aient suggéré arrêter leurs opérations, il est probable qu'ils continuent à cibler des institutions financières.

**Points Clés :**

*   Vol massif de 1.5 milliard d'enregistrements Salesforce impliquant 760 entreprises.
*   Utilisation de jetons OAuth Salesloft Drift compromis comme vecteur d'attaque.
*   Découverte des jetons via l'analyse de code source trouvé dans un dépôt GitHub piraté.
*   Exploitation des données volées pour exfiltrer des secrets et tenter de nouvelles intrusions.
*   Implication de plusieurs groupes de menace connus (ShinyHunters, Scattered Spider, Lapsus$).

**Vulnérabilités :**

*   Compromission de jetons OAuth de la plateforme Salesloft Drift.
*   Exposition de secrets (identifiants, clés d'accès) dans le code source de Salesloft.
*   Potentiel d'accès étendu aux données sensibles des clients via les intégrations Salesforce.

**Recommandations :**

*   Mettre en œuvre l'authentification multi-facteurs (MFA).
*   Appliquer le principe du moindre privilège.
*   Gérer avec soin les applications connectées aux plateformes CRM comme Salesforce.
*   Auditer et sécuriser les dépôts de code source et les secrets qu'ils contiennent.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-claims-15-billion-salesforce-records-stolen-in-drift-hacks/){:target="_blank"}
