---
title: 'NovaCookies Campaigns Abuse Genuine Docusign Notifications to Steal Microsoft 365 Sessions'
date: 2026-08-26
permalink: /posts/2026/08/26/novacookies-campaigns-abuse-genuine-docusign-notifications-to-steal-microsoft-365-sessions/
tags:
- veille-cyber
- hackernews
---
### NovaCookies : Une menace de vol de sessions Microsoft 365 par "Phishing-as-a-Service"

Le kit de phishing **NovaCookies** (variante de Sneaky 2FA) est une plateforme commerciale vendue 320 $/mois, utilisée pour intercepter en temps réel les accès aux comptes Microsoft 365 et Okta. Les attaquants exploitent des notifications légitimes Docusign pour rediriger les victimes vers des pages de connexion frauduleuses, contournant ainsi les mécanismes de sécurité classiques.

#### Points clés
*   **Modèle PhaaS :** Contrairement aux outils précédents, NovaCookies repose sur une infrastructure centralisée gérée par l'opérateur, offrant une solution "clés en main" aux cybercriminels.
*   **Technique AitM (Adversary-in-the-Middle) :** Le kit agit comme un proxy transparent. Une fois que l'utilisateur saisit ses identifiants et son code MFA sur la fausse page, l'attaquant capture la session authentifiée en temps réel.
*   **Evasion :** Utilisation de redirections via des endpoints Microsoft/Google légitimes, de notifications Docusign authentiques (avec le lien malveillant masqué dans le document) et de mécanismes anti-analyse (Cloudflare, détection de debugueurs).
*   **Vecteurs :** Campagnes ciblées sur des organisations internationales, avec des domaines en ".vu" et des libellés usurpant l'identité des services Microsoft.

#### Vulnérabilités exploitées
*   **Abus OAuth :** Exploitation des redirections d'erreurs OAuth pour détourner le flux d'authentification vers une infrastructure contrôlée par l'attaquant.
*   **Confiance aux services tiers :** Exploitation de la réputation de domaines légitimes (Docusign, SharePoint) pour masquer les liens de phishing.
*   *Note : Aucune CVE spécifique n'est associée, il s'agit d'un détournement de fonctionnalités légitimes (design flaw).*

#### Recommandations
*   **Authentification Phishing-Resistant :** Privilégier l'utilisation de clés de sécurité matérielles (FIDO2/WebAuthn) qui ne peuvent pas être capturées par des attaques de type AitM.
*   **Protection des accès (Conditional Access) :** Implémenter des politiques d'accès conditionnel strictes, notamment en restreignant les connexions aux appareils gérés et aux adresses IP connues.
*   **Sensibilisation aux documents :** Former les utilisateurs à la vigilance vis-à-vis des notifications Docusign, même si elles semblent provenir de sources légitimes.
*   **Sécurité E-mail :** Renforcer les outils de filtrage pour inspecter les liens à l'intérieur des pièces jointes (PDF, HTML) et non seulement dans le corps du message.
*   **Surveillance des sessions :** Surveiller les anomalies dans les logs de connexion (ex: changement soudain de localisation géographique, user-agent inhabituel ou accès simultanés).

---
[Source](https://thehackernews.com/2026/08/novacookies-campaigns-abuse-genuine.html){:target="_blank"}
