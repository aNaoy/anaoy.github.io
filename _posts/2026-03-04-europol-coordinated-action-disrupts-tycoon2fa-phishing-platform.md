---
title: 'Europol-coordinated action disrupts Tycoon2FA phishing platform'
date: 2026-03-04
permalink: /posts/2026/03/04/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/
tags:
- veille-cyber
- bleepingcomp
---
**Démantèlement de la plateforme de phishing Tycoon2FA**

Une opération internationale coordonnée par Europol a permis de neutraliser Tycoon2FA, une plateforme majeure de phishing-as-a-service (PhaaS). Cette action, soutenue par des partenaires privés tels que Microsoft, Trend Micro et Cloudflare, a conduit à la saisie de 330 domaines essentiels à l'infrastructure criminelle.

Tycoon2FA, actif depuis au moins août 2023, facilitait le contournement de l'authentification multi-facteurs (MFA) et le compromis de comptes d'environ 100 000 organisations mondiales. Microsoft estimait qu'à mi-2025, la plateforme générait des dizaines de millions de courriels de phishing mensuellement, représentant 60% des tentatives bloquées.

La plateforme fonctionnait comme un système d'interception ("adversary-in-the-middle"), utilisant des serveurs proxy pour capturer en temps réel les identifiants de connexion et les cookies de session des victimes, ciblant notamment les services Microsoft et Google. Elle permettait de détourner des sessions authentifiées et de contourner la MFA, même si l'apparence était celle d'une connexion réussie. Les attaquants pouvaient ainsi usurper l'identité de marques de confiance et conserver un accès, même après une réinitialisation de mot de passe, à moins que les sessions actives ne soient révoquées.

Vendu via Telegram, Tycoon2FA a abaissé le seuil d'accès pour les cybercriminels peu qualifiés souhaitant lancer des attaques sophistiquées à grande échelle.

**Points clés :**

*   Démantèlement de la plateforme de phishing-as-a-service Tycoon2FA.
*   Opération internationale coordonnée par Europol.
*   Saisie de 330 domaines utilisés par la plateforme.
*   Tycoon2FA permettait de contourner la MFA en interceptant les identifiants et les cookies de session.
*   La plateforme ciblait des services tels que Microsoft 365, OneDrive, Outlook, SharePoint et Gmail.
*   Vente de la plateforme via Telegram à bas prix, facilitant l'accès aux cybercriminels.

**Vulnérabilités :**

*   **Contournement de l'authentification multi-facteurs (MFA) :** La plateforme exploitait une faiblesse dans le processus d'authentification pour intercepter les codes MFA ou les cookies de session après une première authentification réussie.

**Recommandations :**

*   **Révocation active des sessions et tokens :** Il est crucial de révoquer explicitement les sessions actives et les tokens d'authentification, même après une réinitialisation de mot de passe, pour contrer les attaques de Tycoon2FA.
*   **Vigilance face au phishing :** Les utilisateurs doivent rester extrêmement prudents face aux e-mails et aux sites web suspects, même s'ils semblent légitimes et demandent des informations d'identification.
*   **Sécurisation des sessions :** Les organisations doivent s'assurer que leurs systèmes de gestion de sessions sont robustes et capables de détecter et de bloquer les activités suspectes, telles que l'utilisation de cookies de session interceptés.
*   **Partage d'informations :** Le partage d'informations sur les menaces entre les forces de l'ordre et le secteur privé est essentiel pour identifier et neutraliser des plateformes criminelles comme Tycoon2FA.

---
[Source](https://www.bleepingcomputer.com/news/security/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/){:target="_blank"}
