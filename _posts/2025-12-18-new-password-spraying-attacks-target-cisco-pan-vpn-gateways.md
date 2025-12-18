---
title: 'New password spraying attacks target Cisco, PAN VPN gateways'
date: 2025-12-18
permalink: /posts/2025/12/18/new-password-spraying-attacks-target-cisco-pan-vpn-gateways/
tags:
- veille-cyber
- bleepingcomp
---
**Attaques automatisées visant les passerelles VPN**

Une campagne automatisée cible les plateformes VPN, notamment Palo Alto Networks GlobalProtect et Cisco SSL VPN, par le biais d'attaques par pulvérisation de mots de passe. Ces attaques, observées en masse, visent à identifier les portails VPN exposés ou faiblement protégés en testant des combinaisons de noms d'utilisateur et de mots de passe courantes.

**Points Clés :**

*   Un pic d'1,7 million de tentatives de connexion sur des portails GlobalProtect a été enregistré en 16 heures, provenant de plus de 10 000 adresses IP uniques.
*   Une activité similaire a été observée sur les passerelles Cisco SSL VPN, avec une augmentation significative du nombre d'adresses IP uniques sondant ces points d'accès.
*   L'origine géographique des attaques semble centralisée, avec une origine identifiée dans l'espace IP de la société 3xK GmbH en Allemagne.
*   Les caractéristiques des requêtes suggèrent des tentatives scriptées de validation de credentials plutôt que l'exploitation de vulnérabilités logicielles spécifiques.
*   Bien qu'une vulnérabilité critique (CVE-2025-20393) ait été signalée par Cisco pour d'autres équipements, aucun lien n'a été établi entre cette vulnérabilité et les attaques observées contre les VPN.

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique (CVE) n'est directement exploitée dans ces attaques. L'objectif est d'exploiter la faiblesse des identifiants de connexion.
*   CVE-2025-20393 (concernant Cisco AsyncOS, non directement liée aux attaques VPN observées).

**Recommandations :**

*   Utiliser des mots de passe forts et uniques.
*   Mettre en place l'authentification multifacteur (MFA).
*   Auditer régulièrement les appliances réseau pour détecter des tentatives de connexion inhabituelles.
*   Bloquer les adresses IP connues pour mener ces sondages d'identifiants.

---
[Source](https://www.bleepingcomputer.com/news/security/new-password-spraying-attacks-target-cisco-pan-vpn-gateways/){:target="_blank"}
