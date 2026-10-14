---
title: 'Ghostscript flaw lets hackers hijack servers via PDF uploads'
date: 2026-10-14
permalink: /posts/2026/10/14/ghostscript-flaw-lets-hackers-hijack-servers-via-pdf-uploads/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans Ghostscript : Risque d'exécution de code à distance

Une vulnérabilité de type dépassement de tampon (heap buffer overflow) dans l'interpréteur Ghostscript expose de nombreux systèmes, dont les plateformes WordPress, à une exécution de code à distance (RCE) via le traitement de fichiers PDF malveillants.

**Points clés :**
*   **Mécanisme :** La faille est déclenchée lors de la génération de vignettes ou de prévisualisations de fichiers PDF contenant des images JPEG 2000 spécifiques, provoquant une corruption de la mémoire.
*   **Portée :** Toutes les versions de Ghostscript comprises entre 9.21 et 10.07.1 sont affectées. Le risque concerne tout système (notamment Linux) utilisant Ghostscript pour traiter des PDF fournis par des utilisateurs.
*   **Statut :** Bien qu'aucune exploitation active dans la nature n'ait été signalée, deux preuves de concept (PoC) ont été développées par des chercheurs.

**Vulnérabilité :**
*   **CVE-2026-39919 :** Dépassement de tampon sur le tas permettant l'injection de code via des fichiers PDF contrefaits.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la version 10.08.0 de Ghostscript (ou les versions rétroportées) fournie par l'éditeur Artifex.
*   **Environnements conteneurisés :** Reconstruire et redéployer les images Docker avec une version de base intégrant le correctif.
*   **Mesures palliatives :** Si la mise à jour est impossible, désactiver le rendu des fichiers PDF dans ImageMagick ou bloquer totalement les téléchargements de fichiers PDF sur le serveur.
*   **Sécurisation WordPress :** S'assurer, via l'hébergeur, que Ghostscript est à jour et restreindre les capacités d'upload de fichiers aux utilisateurs de confiance.

---
[Source](https://www.bleepingcomputer.com/news/security/ghostscript-flaw-lets-hackers-hijack-servers-via-pdf-uploads/){:target="_blank"}
