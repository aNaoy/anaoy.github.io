---
title: 'Apple Patches Everything: February 2026, (Wed, Feb 11th)'
date: 2026-02-12
permalink: /posts/2026/02/12/apple-patches-everything-february-2026-wed-feb-11th/
tags:
- veille-cyber
- sans-isc
---
**Correctifs de Sécurité Apple : Février 2026**

Plusieurs vulnérabilités ont été corrigées par Apple, affectant divers composants de ses systèmes d'exploitation. Les failles identifiées peuvent permettre à des applications malveillantes ou à des attaquants d'accéder à des données sensibles, de provoquer des plantages système, de modifier des fichiers protégés, d'obtenir des privilèges root, voire d'exécuter du code arbitraire dans des cas critiques.

**Points Clés et Vulnérabilités (avec CVE si possible) :**

*   **Accès à des données sensibles :** De nombreuses vulnérabilités (ex: CVE-2025-43403, CVE-2025-43417, CVE-2025-46283, CVE-2026-20603, CVE-2026-20612, CVE-2026-20618, CVE-2026-20619, CVE-2026-20623, CVE-2026-20624, CVE-2026-20625, CVE-2026-20627, CVE-2026-20629, CVE-2026-20630, CVE-2026-20646, CVE-2026-20647, CVE-2026-20648, CVE-2026-20653, CVE-2026-20666, CVE-2026-20669, CVE-2026-20678, CVE-2026-20680, CVE-2026-20681) permettent à des applications de lire des informations utilisateur privées, historiques de navigation, notifications, ou même de découvrir les applications installées.
*   **Plantages et dénis de service :** Plusieurs failles peuvent mener à des arrêts inattendus d'applications ou du système (ex: CVE-2025-43338, CVE-2025-43402, CVE-2026-20605, CVE-2026-20609, CVE-2026-20611, CVE-2026-20616, CVE-2026-20620, CVE-2026-20621, CVE-2026-20654), ou à des attaques par déni de service (ex: CVE-2025-46290, CVE-2026-20602, CVE-2026-20609, CVE-2026-20650, CVE-2026-20652).
*   **Élévation de privilèges :** Des vulnérabilités ont été identifiées permettant à des applications d'obtenir des privilèges root (ex: CVE-2026-20610, CVE-2026-20614, CVE-2026-20615, CVE-2026-20617, CVE-2026-20626, CVE-2026-20658).
*   **Manipulation de fichiers et contournement de sécurité :** Certaines failles permettent la modification de fichiers système (CVE-2025-43537), le contournement des restrictions de sandbox (CVE-2026-20628, CVE-2026-20667, CVE-2026-20677), l'écriture de fichiers arbitraires (CVE-2026-20660), ou l'exploitation de failles dans les pilotes GPU et le Wi-Fi.
*   **Vulnérabilité critique exploitée :** La vulnérabilité CVE-2026-20700, affectant dyld, est particulièrement préoccupante car Apple est conscient d'un rapport indiquant qu'elle aurait pu être exploitée dans une attaque sophistiquée contre des individus ciblés sur des versions antérieures d'iOS. Cette faille peut permettre l'exécution de code arbitraire.

**Recommandations :**

Il est fortement recommandé aux utilisateurs de s'assurer que leurs appareils Apple sont à jour avec les dernières versions logicielles fournies par Apple afin de bénéficier de ces correctifs de sécurité. Les mises à jour logicielles corrigent ces vulnérabilités et protègent contre les menaces potentielles.

---
[Source](https://isc.sans.edu/diary/rss/32706){:target="_blank"}
