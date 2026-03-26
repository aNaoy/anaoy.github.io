---
title: 'TikTok for Business accounts targeted in new phishing campaign'
date: 2026-03-26
permalink: /posts/2026/03/26/tiktok-for-business-accounts-targeted-in-new-phishing-campaign/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de phishing ciblant les comptes TikTok for Business

Une nouvelle campagne de phishing cible les comptes « TikTok for Business » en usurpant des pages de recrutement (type « Google Careers ») pour dérober des identifiants et des jetons de session. Les attaquants utilisent des serveurs mandataires inversés (reverse proxy) capables de contourner l'authentification à deux facteurs (2FA), mettant en péril à la fois le compte TikTok et, potentiellement, le compte Google associé via l'authentification unique (SSO).

**Points clés :**
* **Méthodologie :** Les victimes sont redirigées via des liens Google Storage vers des pages hébergées sur Cloudflare.
* **Technique d'évasion :** Utilisation de Cloudflare Turnstile pour bloquer les robots d'analyse de sécurité et masquer les pages malveillantes.
* **Impact :** Vol d'identifiants et de cookies de session, permettant un détournement complet de compte.
* **Risque SSO :** La compromission d'un compte TikTok lié via Google SSO entraîne souvent le piratage simultané du compte Google.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, cette attaque exploitant principalement l'ingénierie sociale et la manipulation de sessions (Man-in-the-Middle via proxy).

**Recommandations :**
* **Vérification des domaines :** Inspecter systématiquement l'URL avant de saisir des informations, même sur des pages semblant légitimes.
* **Méfiance accrue :** Faire preuve d'une grande prudence face aux offres d'emploi non sollicitées ou aux invitations à des entretiens provenant de sources inconnues.
* **Sécurité des accès :** Privilégier l'utilisation de **clés de sécurité physiques (passkeys)** plutôt que les codes 2FA classiques, car elles offrent une meilleure protection contre les attaques de phishing par proxy.
* **Gestion des accès :** Dissocier, si possible, les comptes professionnels des comptes personnels pour limiter l'impact d'une compromission SSO.

---
[Source](https://www.bleepingcomputer.com/news/security/tiktok-for-business-accounts-targeted-in-new-phishing-campaign/){:target="_blank"}
