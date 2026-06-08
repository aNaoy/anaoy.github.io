---
title: 'Oxford University discloses data breach after careers platform hack'
date: 2026-06-08
permalink: /posts/2026/06/08/oxford-university-discloses-data-breach-after-careers-platform-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données sur la plateforme CareerConnect de l’Université d’Oxford

L'Université d’Oxford a été victime d’une violation de données via son prestataire tiers, **Group GTI**, affectant la plateforme de services de carrière *CareerConnect*. Cette plateforme est également utilisée par d'autres institutions britanniques, telles que le King's College London et l'Université de Manchester.

**Points clés :**
*   **Incident :** Accès non autorisé à la plateforme CareerConnect survenu le 28 mai.
*   **Données exposées :** Noms, prénoms, adresses e-mail et mots de passe chiffrés des utilisateurs utilisant une connexion locale (alumni, chercheurs et employeurs).
*   **Périmètre :** Les systèmes internes de l'université restent sécurisés ; il n'y a aucune preuve d'accès aux fichiers, informations financières ou données des étudiants utilisant le SSO (Single Sign-On).
*   **Objectif :** L'incident semble cibler la collecte d'identifiants pour mener des campagnes de phishing ultérieures.
*   **Contexte :** Il s'agit du second incident de cybersécurité pour l'université cette année, après la compromission du système de gestion d'apprentissage *Canvas* par le groupe ShinyHunters en mai.

**Vulnérabilités :**
*   Aucun CVE spécifique n'a été associé à cette intrusion, le prestataire GTI n'ayant pas encore détaillé la faille technique exacte exploitée. La compromission repose sur une vulnérabilité au sein des systèmes de gestion des accès de la plateforme tierce.

**Recommandations :**
*   **Réinitialisation immédiate :** Les utilisateurs concernés doivent réinitialiser leurs mots de passe de connexion locale.
*   **Vigilance accrue :** Étant donné le risque élevé de campagnes de phishing ciblant les données exfiltrées, les utilisateurs doivent faire preuve d'une prudence extrême face aux e-mails suspects ou aux sollicitations inattendues.
*   **Authentification :** Privilégier systématiquement l'utilisation du Single Sign-On (SSO) lorsqu'il est disponible pour limiter l'exposition des mots de passe locaux.

---
[Source](https://www.bleepingcomputer.com/news/security/oxford-university-discloses-data-breach-after-careerconnect-platform-hack/){:target="_blank"}
