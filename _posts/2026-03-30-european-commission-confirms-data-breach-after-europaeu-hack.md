---
title: 'European Commission confirms data breach after Europa.eu hack'
date: 2026-03-30
permalink: /posts/2026/03/30/european-commission-confirms-data-breach-after-europaeu-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque contre la Commission européenne : Fuite de données via AWS

La Commission européenne a confirmé une violation de données affectant la plateforme web Europa.eu. Le groupe de cybercriminels « ShinyHunters » a revendiqué l'intrusion, affirmant avoir exfiltré plus de 350 Go de données, incluant des bases de données, des contrats et des documents confidentiels. Une partie de ces fichiers (plus de 90 Go) a déjà été publiée sur le dark web.

**Points clés :**
*   **Vecteur d'attaque :** L'incident cible un ou plusieurs comptes Amazon Web Services (AWS) liés à la Commission.
*   **Impact :** Aucune interruption des sites web n'a été constatée. Les systèmes internes de la Commission ne sont pas affectés, mais des données personnelles d'employés ont été compromises.
*   **Auteurs :** Le groupe ShinyHunters, connu pour de nombreuses attaques contre des entreprises majeures via des campagnes de *vishing* ciblant les accès Single Sign-On (SSO).
*   **Contexte :** Il s'agit du second incident majeur signalé par la Commission en peu de temps, après le piratage de sa plateforme de gestion d'appareils mobiles en février.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée dans l'article. La compromission semble résulter d'une faille de sécurité dans la gestion des accès aux comptes cloud (AWS), potentiellement via des techniques d'ingénierie sociale ou de vol d'identifiants SSO, méthodes récurrentes chez les attaquants.

**Recommandations :**
*   **Renforcement de l'authentification :** Généraliser l'authentification multifacteur (MFA) résistante au phishing, en particulier pour les accès aux services cloud et SSO.
*   **Gestion des accès cloud :** Appliquer le principe du moindre privilège sur les comptes AWS et surveiller étroitement les logs d'activité pour détecter toute exfiltration massive de données.
*   **Sécurisation de la Supply Chain :** Accélérer la mise en œuvre de la nouvelle législation européenne sur la cybersécurité visant à mieux contrôler les fournisseurs et renforcer la résilience face aux groupes cybercriminels.

---
[Source](https://www.bleepingcomputer.com/news/security/european-commission-confirms-data-breach-after-europaeu-hack/){:target="_blank"}
