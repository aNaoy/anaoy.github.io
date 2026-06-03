---
title: 'Microsofts Coreutils project brings Linux commands to Windows'
date: 2026-06-03
permalink: /posts/2026/06/03/microsofts-coreutils-project-brings-linux-commands-to-windows/
tags:
- veille-cyber
- bleepingcomp
---
### L'arrivée de Microsoft Coreutils sur Windows

Microsoft a lancé « Coreutils pour Windows », un projet visant à intégrer nativement des outils en ligne de commande Linux au sein de l'écosystème Windows. Basé sur le projet open-source *uutils* (réécriture des GNU Coreutils en Rust), ce paquet facilite l'uniformisation des workflows de développement entre Windows, macOS et Linux sans nécessiter de modifications de scripts.

**Points clés**
*   **Implémentation technique :** Microsoft utilise un binaire unique (`coreutils.exe`) associé à des liens physiques (hardlinks) NTFS pour chaque commande (ex: `ls.exe`, `cp.exe`, `rm.exe`), permettant une gestion simplifiée tout en conservant une syntaxe familière.
*   **Installation :** Disponible via le gestionnaire de paquets Windows : `winget install Microsoft.Coreutils`.
*   **Interopérabilité :** Le projet vise à fluidifier le travail des développeurs en rendant les outils Linux natifs sur Windows.

**Vulnérabilités et limites**
*   **Absence de CVE :** Aucune vulnérabilité n'est associée à cette annonce à ce jour, le projet étant une adaptation d'outils existants.
*   **Conflits de commandes :** Des risques de collision existent entre les utilitaires Linux et les commandes natives de l'Invite de commande ou de PowerShell (ex: `dir`, `more`).
*   **Limites fonctionnelles :** Certains outils système critiques de type POSIX (ex: `chmod`, `chown`, `kill`) sont absents en raison de l'incompatibilité native des signaux POSIX avec l'architecture Windows.

**Recommandations**
*   **Vérification de priorité :** Lors de l'utilisation, validez la priorité d'exécution des commandes en consultant la table de compatibilité fournie par Microsoft, car le comportement varie selon la variable système PATH et les alias PowerShell.
*   **Gestion des permissions :** Soyez vigilant quant aux différences de gestion des droits d'accès et des fins de ligne (line feeds) entre les environnements Linux et Windows, qui peuvent altérer le comportement des scripts.
*   **Tests de scripts :** Testez rigoureusement les scripts existants dans votre environnement spécifique avant un déploiement massif, afin d'identifier tout conflit potentiel avec les outils système déjà présents.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsofts-coreutils-project-brings-linux-commands-to-windows/){:target="_blank"}
