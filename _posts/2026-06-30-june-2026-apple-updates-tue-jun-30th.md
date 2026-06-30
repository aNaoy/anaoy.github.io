---
title: 'June 2026 Apple Updates, (Tue, Jun 30th)'
date: 2026-06-30
permalink: /posts/2026/06/30/june-2026-apple-updates-tue-jun-30th/
tags:
- veille-cyber
- sans-isc
---
### Mises à jour de sécurité Apple : Juin 2026

Apple a déployé des mises à jour correctives pour iOS/iPadOS 26.5.2, macOS Tahoe 26.5.2 et Safari 26.5.2. Cette série de correctifs traite de nombreuses vulnérabilités, principalement concentrées sur les composants web, bien que le noyau système soit également impacté. Aucune des failles répertoriées n'est actuellement signalée comme étant activement exploitée.

**Points clés :**
*   **Périmètre :** Les systèmes iOS, iPadOS et macOS sont concernés. Aucun correctif n'a été publié pour watchOS, tvOS ou visionOS.
*   **Nature des vulnérabilités :** La majorité des failles affectent WebKit, WebRTC, libxslt et les extensions web.
*   **Risques critiques :** Plusieurs vulnérabilités permettent une sortie de sandbox, l'exfiltration de données, la fuite d'informations sensibles (y compris via le presse-papier) ou des corruptions de mémoire.

**Vulnérabilités majeures (Sélection) :**
*   **Noyau et Système :** 
    *   CVE-2026-39868, CVE-2026-43722, CVE-2026-43724 : Risques de terminaison du système, corruption ou accès non autorisé à la mémoire du noyau.
    *   CVE-2026-43743 : Risque de terminaison du système via IOGPUFamily.
*   **Web et Navigation (WebKit/WebRTC) :**
    *   Sortie de sandbox : CVE-2026-43701, CVE-2026-43725.
    *   Exfiltration de données et fuite d'informations : CVE-2026-43700, CVE-2026-43708, CVE-2026-43713, CVE-2026-43732, CVE-2026-43735, CVE-2026-43740.
    *   Hijacking du presse-papier : CVE-2026-43721.
    *   Corruptions de mémoire/Crashs : CVE-2026-43705, CVE-2026-43715, CVE-2026-43718, CVE-2026-43746.

**Recommandations :**
*   **Appliquer les mises à jour :** Procéder immédiatement à l'installation de la version 26.5.2 pour iOS, iPadOS et macOS.
*   **Mise à jour du navigateur :** Assurer que Safari est à jour vers la version 26.5.2 pour neutraliser les vecteurs d'attaque basés sur le contenu web malveillant.

---
[Source](https://isc.sans.edu/diary/rss/33114){:target="_blank"}
