---
title: 'Drawn to Danger: Windows Graphics Vulnerabilities Lead to Remote Code Execution and Memory Exposure'
date: 2025-11-02
permalink: /posts/2025/11/02/drawn-to-danger-windows-graphics-vulnerabilities-lead-to-remote-code-execution-and-memory-exposure/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilités dans le rendu graphique de Windows

Des failles de sécurité ont été découvertes dans l'interface graphique Windows (GDI), permettant potentiellement l'exécution de code à distance et l'exposition d'informations sensibles. Ces vulnérabilités ont été découvertes lors d'une analyse approfondie des fichiers EMF+.

**Points Clés :**

*   Trois vulnérabilités ont été identifiées dans le traitement des métadonnées graphiques au sein de la librairie `GdiPlus.dll`.
*   Les problèmes découverts sont liés à des dépassements de tampon et à des erreurs de gestion de mémoire lors du rendu de certains enregistrements graphiques.
*   Les vulnérabilités ont été corrigées par Microsoft dans les mises à jour de "Patch Tuesday" de mai, juillet et août 2025.

**Vulnérabilités :**

*   **CVE-2025-30388 (Importance : Importante) :** Provoquée par des objets `RECT` invalides dans un enregistrement `EmfPlusSetTSClip`, entraînant un débordement de tampon basé sur le tas. Permet des opérations de lecture/écriture hors limites et potentiellement la divulgation d'informations sensibles. Affecte également Microsoft Office pour Mac et Android.
*   **CVE-2025-53766 (Importance : Critique) :** Causée par des objets `EmfPlusRect` malformés dans un enregistrement `EmfPlusDrawRects`. Conduit à des écritures hors limites dans la mémoire lors de la génération de miniatures, pouvant permettre l'exécution de code arbitraire.
*   **CVE-2025-47984 (Importance : Importante) :** Liée à un enregistrement `EMR_STARTDOC` et à une ancienne vulnérabilité (CVE-2022-35837) avec une correction incomplète. Des champs de chaîne de caractères malformés dans la structure `DOCINFO` peuvent entraîner des lectures hors limites, exposant ainsi des informations sensibles.

**Recommandations :**

*   Appliquer les mises à jour de sécurité Windows fournies par Microsoft, en particulier les correctifs de mai, juillet et août 2025.
*   Les organisations doivent s'assurer que leurs systèmes sont régulièrement mis à jour pour se prémunir contre ces risques.
*   La collaboration continue entre les chercheurs en sécurité et les éditeurs de logiciels est essentielle pour identifier et corriger les vulnérabilités de manière exhaustive.

---
[Source](https://research.checkpoint.com/2025/drawn-to-danger-windows-graphics-vulnerabilities-lead-to-remote-code-execution-and-memory-exposure/){:target="_blank"}
