---
title: 'Apple Patches iOS and macOS, (Mon, Aug 17th)'
date: 2026-08-18
permalink: /posts/2026/08/18/apple-patches-ios-and-macos-mon-aug-17th/
tags:
- veille-cyber
- sans-isc
---
### Campagne massive de correctifs de sécurité Apple : iOS et macOS

Apple a publié une série de correctifs majeurs adressant un nombre important de vulnérabilités critiques affectant les écosystèmes iOS et macOS. Ces failles concernent divers composants système, notamment le noyau (Kernel), le moteur WebKit, le framework ImageIO, ainsi que plusieurs applications intégrées (Contacts, Siri, App Store, Cartes, etc.).

**Points clés :**
*   **Surface d'attaque étendue :** Les vulnérabilités touchent aussi bien le traitement de contenus web (WebKit) que des interactions locales (applications malveillantes, fichiers multimédias corrompus).
*   **Risques critiques :** Plusieurs failles permettent l'exécution de code arbitraire, l'escalade de privilèges (accès root), le contournement de la sandbox, ainsi que l'exfiltration ou la corruption de données sensibles et de la mémoire noyau.
*   **Composants impactés :** Le noyau (Kernel), WebKit/Safari, ImageIO, CoreAudio, CoreMedia, ainsi que des services réseau (mDNSResponder, Telephony).

**Vulnérabilités notables (sélection) :**
*   **Exécution de code arbitraire :** CVE-2026-43776 (AppleDouble), CVE-2026-43818 (ImageIO), CVE-2026-64747 (AVEVideoEncoder), CVE-2026-65346 (ImageIO).
*   **Escalade de privilèges / Sortie de sandbox :** CVE-2026-28973 (libc), CVE-2026-43723 (MediaRemote), CVE-2026-43738 (Maps), CVE-2026-64740 (Game Center), CVE-2026-43821 (WebKit).
*   **Accès aux données et fuites d'informations :** CVE-2026-28958 (WebKit), CVE-2026-43700 (WebKit), CVE-2026-43800 (Siri), CVE-2026-64721/64723 (Kernel).
*   **Sécurité réseau :** CVE-2026-65329 (Telephony - contournement IPSec), CVE-2026-43667 (AirDrop - déni de service).

**Recommandations :**
1.  **Mise à jour immédiate :** Installer sans délai les dernières mises à jour de sécurité fournies par Apple pour iOS et macOS afin de corriger l'ensemble de ces CVE.
2.  **Prudence sur le contenu web :** Éviter de cliquer sur des liens provenant de sources non fiables, étant donné le grand nombre de vulnérabilités ciblant le traitement de contenus web via WebKit.
3.  **Gestion des applications :** Limiter l'installation d'applications provenant de sources tierces ou non vérifiées, ces dernières étant souvent vecteurs d'attaques pour exploiter les failles de privilèges (sandbox).
4.  **Audit des périphériques :** S'assurer que les accessoires connectés et les configurations réseau (Wi-Fi, AirDrop) sont gérés avec les derniers correctifs pour limiter l'exposition à des attaques locales.

---
[Source](https://isc.sans.edu/diary/rss/33254){:target="_blank"}
