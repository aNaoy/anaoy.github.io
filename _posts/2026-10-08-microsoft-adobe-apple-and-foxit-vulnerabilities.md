---
title: 'Microsoft, Adobe, Apple, and Foxit vulnerabilities'
date: 2026-10-08
permalink: /posts/2026/10/08/microsoft-adobe-apple-and-foxit-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
### Vagues de vulnérabilités critiques chez Adobe, Apple, Foxit et Microsoft

L'équipe de recherche Cisco Talos a révélé plusieurs vulnérabilités de sécurité affectant des logiciels largement utilisés. Tous les éditeurs concernés ont publié des correctifs pour remédier à ces failles.

**Points clés :**
*   Les vulnérabilités permettent, selon les cas, une élévation de privilèges, une exécution de code à distance, une divulgation d'informations sensibles ou un déni de service.
*   L'exploitation nécessite généralement l'ouverture de fichiers malveillants ou l'exécution de séquences d'appels API spécifiques.

**Vulnérabilités identifiées :**

*   **Adobe Photoshop :**
    *   CVE-2026-48388 : Élévation de privilèges via la fonction d'installation.
*   **Apple macOS (CoreWLAN) :**
    *   TALOS-2026-2376 : Divulgation d'informations via une séquence d'appels API.
*   **Foxit Reader :**
    *   CVE-2026-57256 : Exécution de code à distance via la manipulation de fichiers malveillants (JavaScript).
    *   CVE-2026-91799 : *Use-after-free* conduisant à une corruption mémoire et exécution de code arbitraire.
*   **Microsoft Windows :**
    *   CVE-2026-50475 (NETIO.sys) : Accès hors limites (*out-of-bounds*) permettant une divulgation d'informations.
    *   CVE-2026-58613 (Cloud Files Mini Filter Driver) : *Use-after-free* permettant l'élévation de privilèges.
    *   CVE-2026-80093 (Cloud Files Mini Filter Driver) : Confusion de type.
    *   CVE-2026-49177 (tcpip.sys) : Lecture hors limites provoquant une divulgation d'informations ou un déni de service.

**Recommandations :**
*   Appliquer immédiatement les dernières mises à jour de sécurité fournies par les éditeurs respectifs.
*   Mettre à jour les ensembles de règles Snort pour détecter les tentatives d'exploitation de ces vulnérabilités.
*   Consulter les rapports détaillés sur le site de [Talos Intelligence](https://talosintelligence.com/vulnerability_reports) pour plus d'informations techniques.

---
[Source](https://blog.talosintelligence.com/microsoft-adobe-apple-and-foxit-vulnerabilities/){:target="_blank"}
