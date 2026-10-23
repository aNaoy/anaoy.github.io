---
title: 'Critical Flaw in Python’s Popular Pillow Image Library Allows Code Execution via a Crafted Image'
date: 2026-10-23
permalink: /posts/2026/10/23/critical-flaw-in-pythons-popular-pillow-image-library-allows-code-execution-via-a-crafted-image/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans la bibliothèque Python Pillow

La bibliothèque de traitement d'images Pillow a publié une mise à jour majeure (version 13.0.0) corrigeant plusieurs vulnérabilités critiques, dont certaines permettent l'exécution de code à distance (RCE). Ces failles touchent des millions de projets traitant des images provenant d'utilisateurs.

**Points clés :**
*   **Vecteurs d'attaque :** Les vulnérabilités sont principalement déclenchées par le traitement de fichiers malveillants ou, dans certains cas, par la manipulation du nom de fichier lors de l'appel à `Image.open()`.
*   **Impact :** Les failles incluent des exécutions de code arbitraire et des dépassements de mémoire tampon (buffer overflows).
*   **Portée :** Les versions de Pillow de 2.6.0 à 12.3.0 sont affectées.

**Vulnérabilités identifiées :**
*   **CVE-2026-112900 (Score 9.2/10) :** Liée à la gestion des fichiers EPS. Pillow passe le nom du fichier à Ghostscript sans vérification, permettant à un attaquant de détourner les commandes système.
*   **CVE-2026-112403 (Score 9.2/10) :** Dépassement de mémoire tampon lors de la création de miniatures (thumbnails) à partir de fichiers JPEG compressés sans perte.
*   **CVE-2026-112393 (Score 9.2/10) :** Dépassement de mémoire tampon lors de l'enregistrement d'images TIFF en mémoire (buffer).
*   **Vulnérabilité FlashPix (FPX) :** Risque d'exécution de code via `Image.open()` si le package `olefile` est installé.

**Recommandations :**
1.  **Mise à jour immédiate :** Passer à la version **Pillow 13.0.0** ou supérieure. Notez que cette version nécessite au minimum Python 3.11.
2.  **Mesures d'atténuation temporaires :**
    *   **EPS :** Désinstaller `Ghostscript` si non nécessaire et éviter d'utiliser des noms de fichiers provenant d'utilisateurs.
    *   **JPEG :** Éviter les méthodes `draft()` et `thumbnail()` sur des fichiers non fiables, ou utiliser `load()` au préalable.
    *   **TIFF :** Éviter d'enregistrer des TIFF provenant d'utilisateurs dans des buffers mémoire (`io.BytesIO`).

---
[Source](https://thehackernews.com/2026/10/critical-flaw-in-pythons-popular-pillow.html){:target="_blank"}
