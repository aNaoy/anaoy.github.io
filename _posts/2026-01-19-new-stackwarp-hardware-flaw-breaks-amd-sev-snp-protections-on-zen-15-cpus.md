---
title: 'New StackWarp Hardware Flaw Breaks AMD SEV-SNP Protections on Zen 1–5 CPUs'
date: 2026-01-19
permalink: /posts/2026/01/19/new-stackwarp-hardware-flaw-breaks-amd-sev-snp-protections-on-zen-15-cpus/
tags:
- veille-cyber
- hackernews
---
## StackWarp : Une nouvelle faille matérielle chez AMD sape les protections SEV-SNP

Une vulnérabilité matérielle, baptisée StackWarp, a été découverte et affecte les processeurs AMD des séries Zen 1 à Zen 5. Développée par des chercheurs du CISPA Helmholtz Center for Information Security, cette faille permet à des attaquants disposant d'un contrôle privilégié sur un serveur hôte d'exécuter du code malveillant au sein de machines virtuelles confidentielles (CVMs). Cela compromet ainsi les garanties d'intégrité offertes par la technologie AMD Secure Encrypted Virtualization with Secure Nested Paging (SEV-SNP).

### Points Clés :

*   **Nature de la faille :** StackWarp exploite une faiblesse matérielle, ciblant un composant d'optimisation de la microarchitecture appelé "stack engine", responsable des opérations accélérées de la pile (stack).
*   **Impact :** La faille permet aux attaquants de manipuler le pointeur de pile d'une CVM, ouvrant la voie au détournement du flux de contrôle et des données. Cela peut mener à l'exécution de code à distance et à une élévation de privilèges à l'intérieur d'une machine virtuelle protégée par SEV-SNP.
*   **Conséquences :** L'attaque peut être utilisée pour extraire des informations sensibles des environnements SEV-SNP, compromettre des CVMs et potentiellement récupérer des clés privées ou contourner des mécanismes d'authentification.
*   **Génération précédente :** Cette découverte fait suite à une précédente étude sur l'attaque CacheWarp (CVE-2023-20592), qui exploitait également des failles matérielles pour contourner SEV-SNP.

### Vulnérabilités :

*   **Nom :** StackWarp
*   **Identifiant CVE :** CVE-2025-29943
*   **Score CVSS v4 :** 4.6 (gravité moyenne)
*   **Type :** Contrôle d'accès inapproprié (Improper Access Control)
*   **Processeurs affectés :** AMD Zen 1 à Zen 5, incluant diverses séries d'EPYC (7003, 8004, 9004, 9005) et EPYC Embedded correspondantes.

### Recommandations :

*   **Mises à jour du microcode :** Installer les mises à jour du microcode et du firmware fournies par les fabricants de matériel. AMD a publié des mises à jour pour cette vulnérabilité en juillet et octobre 2025, avec des correctifs AGESA prévus en avril 2026 pour certaines séries embarquées.
*   **Désactivation temporaire de l'Hyper-Threading :** Pour les opérateurs de serveurs SEV-SNP, il est conseillé de vérifier si l'Hyper-Threading est activé sur les systèmes affectés. Si c'est le cas, une désactivation temporaire peut être envisagée pour les CVMs nécessitant une intégrité particulièrement élevée.
*   **Surveillance des mises à jour :** Rester vigilant quant aux futures mises à jour de sécurité et aux recommandations des fournisseurs de matériel et de logiciels.

---
[Source](https://thehackernews.com/2026/01/new-stackwarp-hardware-flaw-breaks-amd.html){:target="_blank"}
