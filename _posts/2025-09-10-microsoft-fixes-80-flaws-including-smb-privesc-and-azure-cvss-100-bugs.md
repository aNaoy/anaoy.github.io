---
title: 'Microsoft Fixes 80 Flaws — Including SMB PrivEsc and Azure CVSS 10.0 Bugs'
date: 2025-09-10
permalink: /posts/2025/09/10/microsoft-fixes-80-flaws-including-smb-privesc-and-azure-cvss-100-bugs/
tags:
- veille-cyber
- hackernews
---
**Microsoft Corrige 80 Failles de Sécurité Critiques**

Microsoft a publié un ensemble de 80 correctifs de sécurité pour ses logiciels, dont huit jugées critiques et 72 importantes. Aucune de ces vulnérabilités n'a été exploitée activement comme zero-day au moment de la publication. Une majorité des correctifs (38) concerne l'élévation de privilèges, suivis par l'exécution de code à distance (22), la divulgation d'informations (14) et le déni de service (3).

Parmi les vulnérabilités notables :

*   **CVE-2025-55234 (CVSS 8.8)** : Vulnérabilité d'élévation de privilèges dans Windows SMB, qui permettait des attaques par relais si des mesures de sécurité comme la signature SMB n'étaient pas configurées. L'exploitation permettait à un attaquant d'élever ses privilèges. L'entreprise a mis à disposition des outils d'audit pour évaluer la compatibilité des configurations de sécurité SMB.
*   **CVE-2025-54914 (CVSS 10.0)** : Une faille critique dans Azure Networking, permettant l'élévation de privilèges. Cette vulnérabilité, indépendante de l'action utilisateur, est une faille liée au cloud.
*   **CVE-2025-55232 (CVSS 9.8)** : Vulnérabilité d'exécution de code à distance dans Microsoft High Performance Compute (HPC) Pack.
*   **CVE-2025-54918 (CVSS 8.8)** : Un problème d'élévation de privilèges affectant Windows NTLM, potentiellement permettant à un attaquant d'obtenir des privilèges SYSTEM.
*   **CVE-2024-21907 (CVSS 7.5)** : Une faille dans le composant tiers Newtonsoft.Json, utilisé par SQL Server, entraînant un déni de service.
*   **CVE-2025-54911 (CVSS 7.3) et CVE-2025-54912 (CVSS 7.8)** : Deux vulnérabilités d'élévation de privilèges dans BitLocker. Ces correctifs s'ajoutent à quatre autres failles BitLocker corrigées précédemment, qui permettaient de contourner les protections de chiffrement avec un accès physique.

**Recommandations :**

*   Pour renforcer BitLocker, il est conseillé d'activer l'authentification TPM+PIN pour l'amorçage.
*   Pour atténuer les attaques de dégradation sur BitLocker, il est recommandé d'activer la mitigation REVISE.
*   La mise à jour de sécurité intègre également des correctifs pour des vulnérabilités dans Microsoft Edge, notamment CVE-2025-53791 (CVSS 4.7).

D'autres éditeurs ont également publié des mises à jour de sécurité pour leurs produits.

---
[Source](https://thehackernews.com/2025/09/microsoft-fixes-80-flaws-including-smb.html){:target="_blank"}
