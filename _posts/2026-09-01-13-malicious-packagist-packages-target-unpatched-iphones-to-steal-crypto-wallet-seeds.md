---
title: '13 Malicious Packagist Packages Target Unpatched iPhones to Steal Crypto Wallet Seeds'
date: 2026-09-01
permalink: /posts/2026/09/01/13-malicious-packagist-packages-target-unpatched-iphones-to-steal-crypto-wallet-seeds/
tags:
- veille-cyber
- hackernews
---
### Campagne de spyware ciblant les utilisateurs d'iPhone via des thèmes PHP malveillants

Des chercheurs ont identifié 13 thèmes malveillants pour Composer (utilisés principalement par des sites de streaming vietnamiens) servant à injecter du code JavaScript. Ce code redirige les utilisateurs mobiles vers des sites de jeux d'argent et déploie une chaîne d'exploitation sur les iPhone non mis à jour pour voler des données sensibles et des clés privées de portefeuilles de cryptomonnaies.

**Points clés :**
*   **Propagation :** Le code malveillant est intégré dans des thèmes pour OphimCMS et KKPhim distribués via Packagist.
*   **Fonctionnement :** L'attaque détecte la version d'iOS via une iframe cachée et charge un exploit spécifique pour s'échapper de la sandbox WebKit, accéder au noyau (kernel) et obtenir des privilèges de lecture/écriture.
*   **Impact :** Exfiltration massive de données (Keychain, SMS, photos, historique, cookies, etc.) et vol direct de fonds sur des portefeuilles tels que Trust Wallet, Phantom, Tonkeeper et OKX.
*   **Origine :** Liée à une infrastructure d'hébergement sanctionnée (Funnull) et potentiellement opérée par un groupe vietnamien.

**Vulnérabilités exploitées :**
*   **CVE-2025-31277 & CVE-2025-43529 :** Vulnérabilités WebKit.
*   **CVE-2025-43398 / 43510 / 43520 (suspectées) :** Faille d'évasion du noyau (kernel escape) via `AppleM2ScalerCSCDriver`.

**Recommandations :**
*   **Pour les administrateurs de sites :** Auditer immédiatement les thèmes installés (notamment les namespaces `vsmov`, `vsphim`, `haiau009`, `chilltvcms` et `ophimcms`), supprimer les packages suspects et réinitialiser les identifiants compromis.
*   **Pour les utilisateurs d'iPhone :** Maintenir le système à jour vers les versions les plus récentes d'iOS (au-delà de la 18.6.x) pour bénéficier des correctifs de sécurité critiques.

---
[Source](https://thehackernews.com/2026/09/13-malicious-packagist-packages-target.html){:target="_blank"}
