---
title: 'New SparkCat Variant in iOS, Android Apps Steals Crypto Wallet Recovery Phrase Images'
date: 2026-04-03
permalink: /posts/2026/04/03/new-sparkcat-variant-in-ios-android-apps-steals-crypto-wallet-recovery-phrase-images/
tags:
- veille-cyber
- hackernews
---
### Menace mobile : Le malware SparkCat cible les portefeuilles crypto via OCR

Une nouvelle version du malware **SparkCat** a été identifiée sur l'App Store d'Apple et le Google Play Store. Ce cheval de Troie se dissimule dans des applications légitimes (messageries, livraison de repas) pour dérober les phrases de récupération (seed phrases) des portefeuilles de cryptomonnaies stockées dans les galeries photos des utilisateurs.

**Points clés :**
*   **Méthodologie :** Le logiciel malveillant demande l'accès à la galerie photo et utilise un module d'OCR (reconnaissance optique de caractères) pour identifier et exfiltrer les images contenant des phrases mnémotechniques.
*   **Évolution technique :** La version Android utilise désormais la virtualisation de code et des langages multiplateformes pour complexifier l'analyse et contourner les systèmes de détection.
*   **Ciblage :** Initialement concentré sur l'Asie (mots-clés en japonais, coréen et chinois), la variante iOS est désormais capable de détecter les phrases en anglais, élargissant considérablement sa portée géographique.
*   **Origine :** Les chercheurs attribuent cette campagne à des opérateurs sinophones, confirmant une menace active et en constante évolution.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cette campagne, car le malware exploite les autorisations d'accès aux fichiers accordées par les utilisateurs et les fonctionnalités natives du système (accès aux photos).

**Recommandations :**
*   **Gestion des permissions :** Restreindre strictement l'accès aux photos pour les applications tierces, particulièrement celles ne nécessitant pas cette fonctionnalité pour fonctionner.
*   **Sécurisation des données sensibles :** Ne jamais stocker de captures d'écran, de photos ou de fichiers texte contenant des phrases de récupération de portefeuilles crypto sur un appareil connecté.
*   **Protection logicielle :** Installer et maintenir à jour une solution de cybersécurité réputée sur les appareils mobiles pour détecter les comportements malveillants en temps réel.
*   **Vigilance :** Se méfier des applications téléchargées sur les stores, même officielles, si elles demandent des accès disproportionnés par rapport à leur utilité réelle.

---
[Source](https://thehackernews.com/2026/04/new-sparkcat-variant-in-ios-android.html){:target="_blank"}
