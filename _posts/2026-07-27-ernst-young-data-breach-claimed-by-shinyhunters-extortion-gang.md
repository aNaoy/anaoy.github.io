---
title: 'Ernst & Young data breach claimed by ShinyHunters extortion gang'
date: 2026-07-27
permalink: /posts/2026/07/27/ernst-young-data-breach-claimed-by-shinyhunters-extortion-gang/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque sur Ernst & Young : le groupe ShinyHunters impliqué

Le cabinet d'audit Ernst & Young (EY) a été victime d'une violation de données via une attaque par chaîne d'approvisionnement (*supply-chain attack*). Le gang de cybercriminels ShinyHunters a revendiqué l'intrusion, menaçant de publier des données dérobées si aucune rançon n'est versée avant le 31 juillet 2026.

**Points clés :**
* **Origine de l'intrusion :** Compromission d'une plateforme tierce de gestion de tickets informatiques utilisée par le personnel d'EY, permettant d'accéder aux systèmes internes entre le 28 mars et le 12 avril 2024.
* **Données exposées :** Informations personnelles et financières contenues dans des documents fiscaux. Les attaquants affirment également avoir accédé aux environnements Jira, GitHub et Azure de l'entreprise.
* **Revendication :** ShinyHunters soutient avoir exfiltré plus de données que ce que l'entreprise a initialement reconnu, bien que ces affirmations restent à confirmer.
* **Mesures prises par EY :** Sécurisation des systèmes, notification aux autorités fédérales et proposition de services de surveillance d'identité pour les clients impactés.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été mentionnée. La brèche repose sur une vulnérabilité liée à la confiance accordée à un fournisseur tiers, permettant l'usurpation d'identifiants légitimes.

**Recommandations :**
* **Renforcement de la chaîne d'approvisionnement :** Auditer systématiquement la sécurité des solutions tierces et restreindre leurs accès aux données sensibles.
* **Gestion des accès (IAM) :** Appliquer le principe du moindre privilège et imposer l'authentification multifacteur (MFA) sur tous les outils de développement et d'infrastructure (GitHub, Azure, Jira).
* **Monitoring proactif :** Mettre en place une surveillance accrue des activités anormales au sein des outils de gestion des services informatiques (ITSM) et des accès distants pour détecter les intrusions précocement.

---
[Source](https://www.bleepingcomputer.com/news/security/ernst-and-young-data-breach-claimed-by-shinyhunters-extortion-gang/){:target="_blank"}
