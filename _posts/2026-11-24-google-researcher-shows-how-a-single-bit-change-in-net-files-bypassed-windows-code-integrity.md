---
title: 'Google Researcher Shows How a Single Bit Change in .NET Files Bypassed Windows Code Integrity'
date: 2026-11-24
permalink: /posts/2026/11/24/google-researcher-shows-how-a-single-bit-change-in-net-files-bypassed-windows-code-integrity/
tags:
- veille-cyber
- hackernews
---
### Contournement des protections Windows via une manipulation du .NET Framework

Le chercheur de Google Project Zero, James Forshaw, a mis en lumière une faille dans le processus de chargement du .NET Framework. En exploitant un comportement de secours (fallback) lors du chargement des fichiers, il est possible de contourner les protections d'intégrité du code Windows et de charger des fichiers non approuvés en modifiant simplement un seul bit dans l'en-tête du fichier (`IMAGE_FILE_EXECUTABLE_IMAGE`).

**Points clés :**
*   **Méthode :** Utilisation d'une technique de "COM hijacking" pour injecter des fichiers .NET manipulés dans des processus sécurisés.
*   **Impact :** Exécution de code non approuvé au sein de processus protégés, incluant VirtualBox et les processus protégés par l'intégrité du code en mode utilisateur (UMCI) sur Windows 11 S Mode.
*   **Portée :** Il s'agit d'une vulnérabilité locale nécessitant des privilèges faibles, sans interaction utilisateur, mais ne permettant pas une évasion de machine virtuelle vers l'hôte.

**Vulnérabilités identifiées :**
*   **CVE-2026-87268 :** Contours de durcissement des processus dans Oracle VirtualBox (Score : 7.8).
*   **CVE-2026-108398 :** Contournement de l'intégrité du code dans le .NET Framework 4 (Score : 8.8).

**Recommandations :**
*   **Mise à jour VirtualBox :** S'assurer d'utiliser la version 7.2.18 ou ultérieure pour corriger le contournement des processus protégés.
*   **Mise à jour .NET :** Appliquer le correctif cumulatif du 13 octobre 2026 correspondant précisément à votre version de Windows et du .NET Framework via les KB spécifiques listées par Microsoft.

---
[Source](https://thehackernews.com/2026/11/google-researcher-shows-how-single-bit.html){:target="_blank"}
