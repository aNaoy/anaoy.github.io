---
title: 'FFmpeg - Heap-buffer-overflow write in jpeg2000dec'
date: 2025-09-08
permalink: /posts/2025/09/08/ffmpeg-heap-buffer-overflow-write-in-jpeg2000dec/
tags:
- veille-cyber
- zerodaysfans
---
## Vulnérabilité dans FFmpeg avec le décodeur JPEG2000

Une faille de sécurité de type dépassement de tampon sur le tas a été identifiée dans le composant de décodage JPEG2000 de FFmpeg.

**Versions affectées :** Antérieures à FFmpeg 8.0.

**Description du problème :**
La vulnérabilité se situe dans l'atome "Channel Definition cdef" du format JPEG2000. Lorsqu'un format de pixel avec sous-échantillonnage de chrominance est utilisé conjointement avec cet atome, un cas limite peut être déclenché. Cela peut entraîner l'écriture de données prévues pour une composante de luminance de pleine résolution dans une composante de chrominance plus petite, causant ainsi un dépassement du tampon alloué.

**Impact :**
Cette faille est jugée "Élevée" et peut potentiellement permettre à un attaquant d'exécuter du code à distance ou de provoquer un déni de service.

**Points clés :**

*   **Type de vulnérabilité :** Dépassement de tampon sur le tas (Heap-buffer-overflow write).
*   **Composant affecté :** Décodeur JPEG2000 (jpeg2000dec).
*   **Cause :** Interaction entre le sous-échantillonnage de chrominance et l'atome "Channel Definition cdef".
*   **Conséquence :** Écriture de données au-delà des limites du tampon alloué pour les composantes de chrominance.

**Recommandations :**
Il est fortement conseillé de mettre à jour FFmpeg vers une version corrigée (versions postérieures à FFmpeg 8.0).

---
[Source](https://github.com/google/security-research/security/advisories/GHSA-39q3-f8jq-v6mg){:target="_blank"}
