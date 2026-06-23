---
title: 'FFmpeg fixes PixelSmash flaw in widely used video decoder'
date: 2026-06-23
permalink: /posts/2026/06/23/ffmpeg-fixes-pixelsmash-flaw-in-widely-used-video-decoder/
tags:
- veille-cyber
- bleepingcomp
---
### PixelSmash : Vulnérabilité critique dans le décodeur FFmpeg

La vulnérabilité **PixelSmash** (CVE-2026-8461) affecte le décodeur MagicYUV de la bibliothèque `libavcodec` utilisée par FFmpeg. Ce dépassement de tampon (heap out-of-bounds write) survient lors du traitement des tranches vidéo en raison d'un calcul incohérent des hauteurs des plans de chrominance.

**Points clés :**
*   **Vecteurs d'attaque :** Fichiers vidéo malveillants (formats AVI, MKV, MOV). L'exploitation peut être déclenchée par l'ouverture d'un fichier, la génération de miniatures ou l'indexation automatique par des serveurs multimédias.
*   **Impact :** Risque de déni de service (DoS) immédiat. L'exécution de code à distance (RCE) est possible sous certaines conditions (ASLR désactivé ou chaînage avec une autre faille).
*   **Surface d'exposition :** Étendue à de nombreuses applications utilisant FFmpeg, notamment Jellyfin, Kodi, Emby, Nextcloud, PhotoPrism, OBS Studio, ainsi que potentiellement des services de messagerie (Discord, Telegram, Slack).
*   **Exception :** Plex n'est pas vulnérable grâce à une configuration personnalisée limitant les décodeurs activés.

**Vulnérabilité :**
*   **CVE-2026-8461 :** Score de criticité élevé (8.8).

**Recommandations :**
*   **Mise à jour :** Installer la version **8.1.2** de FFmpeg, qui corrige nativement ce défaut.
*   **Application :** Mettre à jour les serveurs multimédias (comme Jellyfin) et les logiciels dépendants de FFmpeg vers leurs versions les plus récentes.
*   **Atténuation :** Pour les administrateurs de serveurs, envisager la mise en place de listes de blocage de formats de fichiers si l'application le permet, en attendant les mises à jour logicielles.

---
[Source](https://www.bleepingcomputer.com/news/security/ffmpeg-fixes-pixelsmash-flaw-in-widely-used-video-decoder/){:target="_blank"}
