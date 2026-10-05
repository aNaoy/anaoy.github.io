---
title: 'New Dell System Update flaw lets hackers gain root privileges'
date: 2026-10-05
permalink: /posts/2026/10/05/new-dell-system-update-flaw-lets-hackers-gain-root-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans l'outil Dell System Update (DSU)

Dell a publié des correctifs urgents pour plusieurs vulnérabilités affectant son outil de déploiement *System Update* (DSU), utilisé pour gérer les mises à jour de firmware et de BIOS sur les serveurs PowerEdge. Ces failles permettent à des attaquants non authentifiés de prendre le contrôle total des systèmes impactés.

**Points clés :**
*   **Risque :** Exécution de code arbitraire avec privilèges root, compromission complète du système d'exploitation.
*   **Historique :** Dell fait face à une recrudescence d'exploits de la part de groupes de cyberespionnage étatiques ciblant ses produits.
*   **Outils concernés :** Dell System Update (DSU) et Dell Container Storage Modules (CSM).

**Vulnérabilités identifiées :**
*   **CVE-2026-86360 :** Faille critique de type *path traversal* dans DSU permettant l'accès au système de fichiers et l'exécution de code à distance.
*   **CVE-2026-63697 & CVE-2026-71168 :** Failles de haute sévérité permettant l'exécution de code à distance.
*   **CVE-2026-86361 & CVE-2026-86362 :** Failles de haute sévérité permettant l'élévation de privilèges.
*   **CVE-2026-63688 & CVE-2026-63692 :** Vulnérabilités de sévérité maximale dans les *Container Storage Modules* (CSM).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs en passant l'outil Dell System Update (DSU) à la version **2.3.0.0 ou ultérieure**.
*   **Correction prioritaire :** Mettre à jour également les modules de stockage (CSM) pour corriger les failles critiques identifiées simultanément.

---
[Source](https://www.bleepingcomputer.com/news/security/new-dell-system-update-flaw-lets-hackers-gain-root-privileges/){:target="_blank"}
