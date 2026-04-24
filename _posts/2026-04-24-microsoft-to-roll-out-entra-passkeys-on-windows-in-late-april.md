---
title: 'Microsoft to roll out Entra passkeys on Windows in late April'
date: 2026-04-24
permalink: /posts/2026/04/24/microsoft-to-roll-out-entra-passkeys-on-windows-in-late-april/
tags:
- veille-cyber
- bleepingcomp
---
### Déploiement des passkeys Microsoft Entra sur Windows

Microsoft déploiera fin avril 2026 le support des passkeys pour l'authentification sans mot de passe sur les ressources protégées par Microsoft Entra, avec une disponibilité générale prévue pour mi-juin 2026. Cette fonctionnalité permet d'utiliser les méthodes Windows Hello (visage, empreinte digitale ou code PIN) pour s'authentifier sur des appareils Windows, qu'ils soient gérés par l'entreprise, personnels ou partagés.

**Points clés :**
*   **Protection contre le phishing :** Les passkeys sont liés cryptographiquement à l'appareil et ne sont jamais transmis sur le réseau, rendant les tentatives de vol de preuves d'authentification inefficaces.
*   **Flexibilité accrue :** Contrairement à *Windows Hello for Business*, cette solution ne nécessite pas que l'appareil soit joint ou enregistré dans Microsoft Entra ID.
*   **Portée :** Couvre les accès aux ressources Microsoft Entra depuis des environnements non gérés, comblant une faille de sécurité majeure liée à l'usage des mots de passe sur les appareils personnels/partagés.

**Vulnérabilités adressées :**
*   L'article ne mentionne pas de CVE spécifique, mais cible directement les attaques par **phishing**, **brute-force** et **credential stuffing** (bourrage d'identifiants), ainsi que les abus de systèmes SSO (Single Sign-On) qui ont récemment été la cible de cyberattaques massives.

**Recommandations :**
*   **Configuration :** Les administrateurs doivent activer l'option « Microsoft Entra ID with passkeys » dans les politiques de méthodes d'authentification.
*   **Contrôle :** Utiliser les politiques d'accès conditionnel (Conditional Access) pour définir strictement les conditions d'utilisation de ces passkeys.
*   **Stratégie globale :** S'inscrire dans l'initiative « Secure Future » de Microsoft en généralisant l'authentification multifacteur (MFA) et en privilégiant, dès que possible, une approche « sans mot de passe » par défaut pour tous les comptes.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-roll-out-entra-passkeys-on-windows-in-late-april/){:target="_blank"}
