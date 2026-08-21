---
title: 'Microsoft blames Windows gaming issues on RGB lighting devices'
date: 2026-08-21
permalink: /posts/2026/08/21/microsoft-blames-windows-gaming-issues-on-rgb-lighting-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Instabilité des jeux sous Windows 11 liée aux périphériques RGB

Depuis la mise à jour d'août 2026 (KB5121003), les utilisateurs de Windows 11 (versions 24H2 et 25H2) font face à des plantages, des gels de système, des erreurs « EXCEPTION_ACCESS_VIOLATION » et des redémarrages intempestifs lors du lancement de certains jeux.

**Points clés :**
*   **Cause identifiée :** L'incident est lié à des pilotes ou composants de périphériques dotés d'un éclairage RGB, spécifiquement le fichier `inpoutx64.sys`.
*   **Origine technique :** Les changements apportés par la mise à jour KB5121003 au niveau du pilote du noyau Windows sont incompatibles avec ce fichier, provoquant des conflits lors de l'exécution de titres comme *The Finals* ou *ARC Raiders*.
*   **Vulnérabilité :** Aucune CVE n'est associée à cet incident, car il s'agit d'un problème de stabilité logicielle (incompatibilité de pilote) et non d'une faille de sécurité exploitable.

**Recommandations :**
*   **Attente d'un correctif officiel :** Microsoft enquête actuellement pour résoudre le conflit entre les composants RGB et le noyau Windows.
*   **Solution de contournement temporaire :** En cas d'urgence, le studio Embark suggère de supprimer le service associé et de retirer le fichier `inpoutx64.sys` du dossier des pilotes Windows. *Attention : cette manipulation peut désactiver les fonctionnalités de contrôle de l'éclairage RGB de vos périphériques.*

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-blames-windows-gaming-issues-on-rgb-lighting-devices/){:target="_blank"}
