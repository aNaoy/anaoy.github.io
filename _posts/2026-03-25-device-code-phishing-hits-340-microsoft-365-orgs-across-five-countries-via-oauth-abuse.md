---
title: 'Device Code Phishing Hits 340+ Microsoft 365 Orgs Across Five Countries via OAuth Abuse'
date: 2026-03-25
permalink: /posts/2026/03/25/device-code-phishing-hits-340-microsoft-365-orgs-across-five-countries-via-oauth-abuse/
tags:
- veille-cyber
- hackernews
---
### Campagne de phishing par code d'appareil visant Microsoft 365

Une vaste campagne de phishing exploitant le flux d'autorisation OAuth (Device Code Flow) cible actuellement plus de 340 organisations Microsoft 365 à travers le monde. Cette attaque repose sur l'utilisation de plateformes légitimes (Railway.com, Cloudflare Workers, Vercel) et de services de redirection sécurisés pour contourner les filtres de messagerie et tromper les utilisateurs.

**Points clés :**
*   **Mécanisme :** L'attaquant génère un code d'appareil via l'API Microsoft. La victime est incitée à saisir ce code sur une fausse page de connexion. Une fois le code validé par l'utilisateur (avec ses identifiants et 2FA), l'attaquant récupère des jetons d'accès et de rafraîchissement persistants.
*   **Persistance :** Les jetons d'accès obtenus restent valides même après une réinitialisation du mot de passe de la victime.
*   **Infrastructure :** Utilisation intensive de la plateforme Railway pour l'hébergement des moteurs de phishing et de Cloudflare pour masquer les redirections.
*   **Origine :** Attribuée à la plateforme de phishing-as-a-service (PhaaS) nommée "EvilTokens", active sur Telegram.

**Vulnérabilités :**
*   **Exploitation du flux OAuth :** Il ne s'agit pas d'une vulnérabilité logicielle avec CVE, mais d'un abus de la conception légitime du flux *OAuth 2.0 Device Code Flow*. Cette technique exploite la confiance accordée aux domaines Microsoft (`microsoft.com/devicelogin`).

**Recommandations :**
*   **Audit des accès :** Analyser les journaux de connexion (sign-in logs) à la recherche d'activités suspectes provenant d'infrastructures cloud (notamment les adresses IP de Railway.com mentionnées dans l'article).
*   **Réponse aux incidents :** En cas de compromission, révoquer immédiatement tous les jetons de rafraîchissement (refresh tokens) des utilisateurs affectés.
*   **Filtrage réseau :** Bloquer les connexions sortantes vers les infrastructures d'hébergement suspectes (IP Railway identifiées) si elles ne sont pas nécessaires aux activités de l'entreprise.
*   **Sensibilisation :** Éduquer les utilisateurs sur les risques liés aux demandes d'autorisation par "code d'appareil", une méthode inhabituelle pour une connexion standard.

---
[Source](https://thehackernews.com/2026/03/device-code-phishing-hits-340-microsoft.html){:target="_blank"}
