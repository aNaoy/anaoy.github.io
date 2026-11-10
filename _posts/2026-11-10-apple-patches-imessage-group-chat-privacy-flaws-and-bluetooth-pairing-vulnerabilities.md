---
title: 'Apple Patches iMessage Group Chat Privacy Flaws and Bluetooth Pairing Vulnerabilities'
date: 2026-11-10
permalink: /posts/2026/11/10/apple-patches-imessage-group-chat-privacy-flaws-and-bluetooth-pairing-vulnerabilities/
tags:
- veille-cyber
- hackernews
---
### Sécurisation des communications et des connexions sans fil chez Apple

Apple a déployé des mises à jour correctives pour remédier à plusieurs failles critiques affectant iMessage, la bibliothèque de compression Brotli et les protocoles de connectivité Bluetooth/AirPlay.

**Points clés :**
*   **iMessage :** Deux vulnérabilités majeures permettaient à des attaquants distants de s'infiltrer dans des conversations de groupe ou d'accéder à l'historique des messages antérieurs à leur arrivée.
*   **Brotli :** La bibliothèque de compression de Google contient une faille de corruption de mémoire, déjà exploitée activement selon la CISA.
*   **Bluetooth :** Plusieurs vulnérabilités permettent l'appairage non autorisé, le contournement des limites de tentatives de codes d'appairage et la corruption de mémoire.
*   **Disparités :** Tous les appareils Apple ne bénéficient pas immédiatement de ces correctifs selon les versions d'OS installées.

**Vulnérabilités identifiées :**
*   **CVE-2026-113961 :** Problème d'autorisation permettant à un attaquant distant de rejoindre une discussion de groupe iMessage.
*   **CVE-2026-113960 :** Accès non autorisé aux messages précédents lors de l'ajout à une discussion iMessage.
*   **CVE-2026-111497 :** Écriture hors limites (*out-of-bounds write*) dans le décodeur Brotli, susceptible d'entraîner une corruption de mémoire.

**Recommandations :**
*   **Mise à jour immédiate :** Installez les dernières versions disponibles d'iOS, iPadOS et watchOS dès que possible.
*   **Vérification de compatibilité :** Étant donné que certaines versions (notamment iOS 18.7.12 et watchOS 26.6.1) ne mentionnent pas explicitement tous les correctifs, il est conseillé de rester attentif aux futures mises à jour système si votre appareil est concerné par ces versions.
*   **Prudence :** En l'absence de solution de contournement (workaround) officielle, limitez l'utilisation du Bluetooth dans des lieux publics si vous n'êtes pas sur une version corrigée.

---
[Source](https://thehackernews.com/2026/11/apple-patches-imessage-group-chat.html){:target="_blank"}
