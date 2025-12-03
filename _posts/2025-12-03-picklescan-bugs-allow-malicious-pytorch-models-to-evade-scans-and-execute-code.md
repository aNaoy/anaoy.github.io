---
title: 'Picklescan Bugs Allow Malicious PyTorch Models to Evade Scans and Execute Code'
date: 2025-12-03
permalink: /posts/2025/12/03/picklescan-bugs-allow-malicious-pytorch-models-to-evade-scans-and-execute-code/
tags:
- veille-cyber
- hackernews
---
**Faille dans Picklescan : Les modèles PyTorch malveillants contournent la sécurité**

Des vulnérabilités critiques ont été découvertes dans Picklescan, un utilitaire open-source conçu pour analyser les fichiers pickle et prévenir l'exécution de code malveillant, notamment dans le contexte de modèles PyTorch. Ces failles permettent à des acteurs malveillants de masquer du code dangereux dans des modèles et de contourner les protections de l'outil, ouvrant la voie à des attaques de la chaîne d'approvisionnement.

**Points clés :**

*   Picklescan analyse les fichiers pickle au niveau bytecode pour détecter des importations ou des appels de fonctions suspects.
*   Les fichiers pickle, utilisés par PyTorch pour enregistrer et charger des modèles, peuvent exécuter du code arbitraire lors de leur chargement.
*   Les failles découvertes permettent de tromper Picklescan, de faire passer des modèles infectés pour sûrs et d'exécuter du code malveillant.
*   Ces vulnérabilités illustrent les défis liés à la complexité croissante des bibliothèques d'IA et à l'adaptation des outils de sécurité.

**Vulnérabilités :**

*   **CVE-2025-10155** (score CVSS : 9.3/7.8) : Permet de contourner le scan en utilisant des extensions de fichiers courantes pour PyTorch (.bin, .pt) au lieu d'un fichier pickle standard.
*   **CVE-2025-10156** (score CVSS : 9.3/7.5) : Permet de désactiver l'analyse des archives ZIP en introduisant une erreur de contrôle de redondance cyclique (CRC).
*   **CVE-2025-10157** (score CVSS : 9.3/8.3) : Permet de contourner la vérification des "unsafe globals" de Picklescan, menant à l'exécution de code arbitraire en contournant la liste noire des importations dangereuses.
*   **CVE-2025-46417** (score CVSS : 7.5/7.1) : Permet de contourner la liste noire de Picklescan et d'exfiltrer des informations sensibles via DNS lorsque le modèle est chargé, en utilisant des modules Python légitimes comme `linecache` et `ssl`.

**Recommandations :**

*   Mettre à jour Picklescan vers la version **0.0.31** ou supérieure, où ces vulnérabilités ont été corrigées.
*   Les organisations doivent envisager des approches de sécurité plus robustes, telles qu'un proxy de sécurité pour les modèles d'IA, qui analyse activement les nouveaux modèles et est continuellement mis à jour par des experts.
*   Être conscient des limites des outils de sécurité conventionnels face à l'évolution rapide des technologies d'IA.

---
[Source](https://thehackernews.com/2025/12/picklescan-bugs-allow-malicious-pytorch.html){:target="_blank"}
