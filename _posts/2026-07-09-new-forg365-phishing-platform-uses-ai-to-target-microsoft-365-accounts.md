---
title: 'New Forg365 phishing platform uses AI to target Microsoft 365 accounts'
date: 2026-07-09
permalink: /posts/2026/07/09/new-forg365-phishing-platform-uses-ai-to-target-microsoft-365-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Forg365 : Une nouvelle plateforme de phishing automatisée ciblant Microsoft 365

Forg365 est une plateforme de "Phishing-as-a-Service" (PhaaS) sophistiquée conçue pour compromettre les comptes Microsoft 365. Elle intègre l'intelligence artificielle pour générer des leurres personnalisés, rendant ses campagnes d'e-mails particulièrement difficiles à détecter.

**Points clés :**
*   **Intégration d'IA :** Un tableau de bord tout-en-un permet aux attaquants de générer des emails de phishing, de gérer des campagnes et de surveiller les boîtes mail compromises via des mots-clés prédéfinis.
*   **Persistance via extension :** L'outil « ForgCookie » est une extension de navigateur qui rafraîchit automatiquement les cookies de session Microsoft, garantissant aux attaquants un accès permanent sans nécessité de ré-authentification.
*   **Infrastructure mature :** Utilisation de services légitimes (Amazon SES, Cloudflare Pages) pour distribuer les emails et héberger les pages de phishing, contournant ainsi les filtres de sécurité classiques.
*   **Protection anti-analyse :** La plateforme intègre des mécanismes robustes de détection de bots, de sandboxes et de VPN pour empêcher les chercheurs en sécurité d'accéder à son administration.

**Vulnérabilités exploitées :**
*   **Device Code Phishing :** Exploitation du flux d'authentification OAuth 2.0 destiné aux appareils sans navigateur (IoT, TV connectées) pour inciter les victimes à autoriser un appareil contrôlé par l'attaquant.
*   **AiTM (Adversary-in-the-Middle) :** Interception en temps réel des jetons de session et des cookies d'authentification, rendant inefficace le MFA (authentification multi-facteurs) classique.
*   *Note : Aucune CVE spécifique n'est associée, ces attaques reposent sur l'abus détourné de fonctionnalités légitimes de Microsoft.*

**Recommandations :**
*   **Restreindre l'authentification :** Désactiver ou limiter strictement l'utilisation de l'authentification par « code d'appareil » (Device Code) au sein de l'organisation.
*   **Surveillance proactive :** Auditer régulièrement les journaux Microsoft Entra à la recherche d'événements de connexion par code d'appareil, de création de règles de messagerie suspectes ou d'octrois d'applications OAuth inhabituels.
*   **Réponse immédiate :** En cas de compromission avérée, révoquer immédiatement toutes les sessions actives et les jetons d'accès des utilisateurs concernés.

---
[Source](https://www.bleepingcomputer.com/news/security/new-forg365-phishing-platform-uses-ai-to-target-microsoft-365-accounts/){:target="_blank"}
