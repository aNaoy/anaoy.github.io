---
title: 'Nissan discloses employee data breach linked to Oracle zero-day attacks'
date: 2026-06-30
permalink: /posts/2026/06/30/nissan-discloses-employee-data-breach-linked-to-oracle-zero-day-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez Nissan : Exploitation d'une faille zero-day Oracle

Nissan a été victime d'un vol de données touchant ses employés actuels et anciens en Amérique du Nord et au Brésil. L'attaque, attribuée au groupe cybercriminel ShinyHunters, a été rendue possible par l'exploitation d'une vulnérabilité critique affectant le logiciel Oracle PeopleSoft utilisé par l'entreprise pour la gestion du personnel.

**Points clés :**
* **Cible :** Nissan Americas et des centaines d'autres organisations.
* **Données exposées :** Informations de contact, données bancaires, numéros de sécurité sociale, dossiers fiscaux et informations sur les bénéficiaires.
* **Auteurs :** Le groupe d'extorsion ShinyHunters, responsable de nombreuses campagnes de vol de données massives (notamment dans le secteur de l'éducation).

**Vulnérabilité exploitée :**
* **CVE-2026-35273 :** Faille critique dans Oracle PeopleSoft PeopleTools. Utilisée initialement comme "zero-day", elle a permis une exécution de code ou un accès non autorisé aux instances PeopleSoft avant la mise en ligne des correctifs d'urgence par Oracle.

**Recommandations et mesures prises :**
* **Sécurisation des accès :** Restreinte aux ordinateurs du réseau interne ou aux connexions VPN sécurisées pour la consultation des fiches de paie et les modifications de dépôt direct.
* **Renforcement des identités :** Mise en œuvre de mesures de vérification d'identité supplémentaires pour toute requête relative à la paie.
* **Protection des victimes :** Nissan propose des services gratuits de surveillance du crédit et du dark web aux personnes affectées.
* **Conseil général :** Les entreprises utilisant Oracle PeopleSoft doivent s'assurer que les correctifs d'urgence fournis par Oracle suite à la divulgation de la CVE-2026-35273 sont intégralement appliqués.

---
[Source](https://www.bleepingcomputer.com/news/security/nissan-discloses-employee-data-breach-linked-to-oracle-zero-day-attacks/){:target="_blank"}
