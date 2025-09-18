---
title: 'SilentSync RAT Delivered via Two Malicious PyPI Packages Targeting Python Developers'
date: 2025-09-18
permalink: /posts/2025/09/18/silentsync-rat-delivered-via-two-malicious-pypi-packages-targeting-python-developers/
tags:
- veille-cyber
- hackernews
---
**Des paquets malveillants sur PyPI diffusent le RAT SilentSync**

Deux paquets Python malveillants, "sisaws" et "secmeasure", ont été découverts sur le dépôt PyPI. Ces paquets, désormais retirés, étaient utilisés pour distribuer un cheval de Troie d'accès à distance (RAT) nommé SilentSync sur les systèmes Windows. L'attaquant a utilisé une technique de "typosquatting" en imitant des noms de paquets légitimes (SISA pour "sisaws").

**Points clés :**

*   Deux paquets malveillants ("sisaws", "secmeasure") ont été trouvés sur PyPI.
*   Ils distribuent le RAT SilentSync.
*   SilentSync cible les systèmes Windows, mais possède des capacités pour Linux et macOS.
*   L'attaque s'inscrit dans le cadre d'une menace sur la chaîne d'approvisionnement logicielle.

**Fonctionnalités de SilentSync :**

*   Exécution de commandes à distance.
*   Vol de données de navigateurs (identifiants, historique, cookies).
*   Capture d'écran.
*   Exfiltration de fichiers et de répertoires (compressés en ZIP).
*   Auto-effacement des artefacts pour éviter la détection.

**Vulnérabilités :**

Aucun identifiant CVE spécifique n'est mentionné dans l'article pour ces paquets ou le RAT. L'exploitation repose sur l'ingénierie sociale (confiance dans les dépôts de paquets) et la faiblesse des contrôles de sécurité dans la chaîne d'approvisionnement.

**Recommandations :**

*   Être vigilant lors de l'installation de paquets depuis des dépôts publics.
*   Vérifier la légitimité et la réputation des paquets avant leur utilisation.
*   Mettre en place des outils de sécurité pour détecter et bloquer les malwares.
*   Restreindre les dépendances aux sources fiables et vérifiées lorsque cela est possible.

---
[Source](https://thehackernews.com/2025/09/silentsync-rat-delivered-via-two.html){:target="_blank"}
