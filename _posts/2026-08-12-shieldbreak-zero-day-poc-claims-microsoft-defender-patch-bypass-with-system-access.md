---
title: 'ShieldBreak Zero-Day PoC Claims Microsoft Defender Patch Bypass With SYSTEM Access'
date: 2026-08-12
permalink: /posts/2026/08/12/shieldbreak-zero-day-poc-claims-microsoft-defender-patch-bypass-with-system-access/
tags:
- veille-cyber
- hackernews
---
### ShieldBreak : Une faille zero-day contourne le correctif de Microsoft Defender

Le chercheur en sécurité « Chaotic Eclipse » a révélé l'existence de **ShieldBreak**, une vulnérabilité zero-day agissant comme un contournement complet du correctif appliqué à la faille « RoguePlanet ». Cette vulnérabilité permet à un attaquant d'obtenir des privilèges de niveau **SYSTEM** et d'exécuter du code arbitraire sur Windows 11 25H2 et Windows Server 2025.

**Points clés :**
*   **Contournement de patch :** ShieldBreak exploite une insuffisance dans la correction de CVE-2026-50656.
*   **Impact :** Élévation de privilèges avec un taux de réussite de 100 % selon le chercheur.
*   **Vulnérabilité initiale :** RoguePlanet (CVE-2026-50656) est une condition de course située dans le moteur de protection contre les logiciels malveillants de Microsoft (`mpengine.dll`).
*   **Contexte étendu :** Microsoft a récemment corrigé d'autres vulnérabilités critiques, notamment **CVE-2026-62832** (LegacyHive, élévation de privilèges via le service de profil utilisateur) et **CVE-2026-68820** (exploitation active du pilote WinSock).

**Vulnérabilités mentionnées :**
*   **CVE-2026-50656 (RoguePlanet) :** Élevation de privilèges dans Microsoft Defender (CVSS 7.8).
*   **CVE-2026-62832 (LegacyHive) :** Faille dans le service de profil utilisateur (CVSS 7.8).
*   **CVE-2026-68820 :** Faille dans le pilote WinSock, actuellement exploitée activement (CVSS 7.0).
*   **CVE-2026-72971 :** Faille de falsification dans le pilote `unionfs.sys` (CVSS 5.5).

**Recommandations :**
*   Appliquer immédiatement les correctifs fournis par Microsoft lors du cycle de mise à jour d'août 2026.
*   Pour la faille **CVE-2026-68820**, la CISA impose aux agences fédérales américaines une mise en conformité avant le 25 août 2026, soulignant le caractère critique de cette vulnérabilité.
*   Surveiller les prochaines annonces de Microsoft concernant ShieldBreak, l'éditeur étant actuellement en phase d'investigation sur ce signalement.

---
[Source](https://thehackernews.com/2026/08/shieldbreak-zero-day-poc-claims.html){:target="_blank"}
