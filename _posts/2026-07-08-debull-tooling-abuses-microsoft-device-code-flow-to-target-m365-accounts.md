---
title: 'DEBULL Tooling Abuses Microsoft Device-Code Flow to Target M365 Accounts'
date: 2026-07-08
permalink: /posts/2026/07/08/debull-tooling-abuses-microsoft-device-code-flow-to-target-m365-accounts/
tags:
- veille-cyber
- hackernews
---
### Menace émergente : L'essor du phishing par code d'appareil (Device Code Phishing)

L'écosystème cybercriminel s'est récemment professionnalisé autour d'une technique exploitant le flux d'autorisation par code d'appareil OAuth 2.0 pour compromettre les comptes Microsoft 365. L'outil **DEBULL**, utilisé par des acteurs malveillants, illustre cette tendance où les méthodes complexes de Storm-2372 sont désormais packagées sous forme de services « Phishing-as-a-Service » (PhaaS).

**Points clés :**
*   **Mécanisme d'abus :** Contrairement au phishing classique, cette attaque utilise le véritable portail de connexion Microsoft. L'attaquant force la victime à entrer un code d'appareil légitime, ce qui autorise la session de l'attaquant sans nécessiter de mot de passe ni contourner directement le MFA.
*   **Infrastructure modulaire :** Des outils comme DEBULL, ARToken ou Tycoon 2FA permettent aux cybercriminels de déployer des tableaux de bord automatisés pour gérer le vol de jetons, l'exfiltration de données (email, OneDrive, SharePoint) et l'automatisation de la compromission d'emails professionnels (BEC) via l'IA.
*   **Propagation :** Les attaques utilisent souvent le « saut de compte » (ATO jumping), où un compte déjà compromis envoie des liens malveillants vers ses contacts. L'infrastructure repose parfois sur des sites web légitimes compromis pour orchestrer les étapes du vol de jeton.

**Vulnérabilités exploitées :**
*   Il ne s'agit pas d'une vulnérabilité logicielle (CVE) classique, mais d'un **abus de conception du flux d'authentification OAuth 2.0 Device Authorization Grant**. En détournant un processus conçu pour les appareils sans interface (TV, imprimantes), les attaquants contournent les mesures de protection habituelles.

**Recommandations de sécurité :**
*   **Limiter les accès :** Restreindre l'utilisation du flux de code d'appareil dans les politiques d'accès conditionnel de Microsoft Entra.
*   **Sensibilisation :** Éduquer les utilisateurs sur les risques liés à la saisie de codes d'appareil, une procédure qui ne devrait presque jamais être requise dans un environnement bureautique standard.
*   **Surveillance :** Surveiller les journaux d'audit pour détecter des connexions inhabituelles via le flux « Device Code » et examiner les applications autorisées dans l'environnement Microsoft 365 pour repérer les jetons suspects.
*   **Protection des comptes :** Appliquer une authentification forte (Phishing-resistant MFA, telle que FIDO2/WebAuthn) qui protège contre les attaques de type « adversary-in-the-middle » ou de détournement de session.

---
[Source](https://thehackernews.com/2026/07/debull-tooling-abuses-microsoft-device.html){:target="_blank"}
