---
title: 'Novinarya: An Android stealer that hides its live C2 in a shop bio'
date: 2026-10-08
permalink: /posts/2026/10/08/novinarya-an-android-stealer-that-hides-its-live-c2-in-a-shop-bio/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de Novinarya : Un malware Android utilisant des places de marché comme relais C2

Novinarya est un logiciel malveillant ciblant les applications bancaires et de cryptomonnaie en Iran. Il se distingue par une architecture multi-couches complexe et une méthode innovante de résolution de son serveur de commande et contrôle (C2).

#### Points clés
*   **Architecture native :** L'application installe un chargeur léger qui dépaquette une charge utile Basic4Android (B4A) via un algorithme RC4 et zlib, dissimulée dans les actifs de l'APK.
*   **Ciblage :** Le malware énumère les applications installées pour identifier 81 cibles financières spécifiques (portefeuilles crypto et banques iraniennes).
*   **Vol de données :** Il utilise des *WebView* avec injection de JavaScript pour capturer des identifiants (phishing), et intercepte les notifications et les SMS pour dérober des codes OTP et des soldes de comptes bancaires.
*   **Résolution C2 via "Dead Drop" :** Le C2 n'est pas présent dans le code. Le malware déchiffre une URL cachée dans le manifeste (clé `X_ROUTES`), qui pointe vers la biographie d'un profil d'utilisateur sur une place de marché légitime (Basalam). La biographie contient un blob chiffré qui, une fois déchiffré, révèle l'adresse dynamique du C2 (`hxxp://theapi.the-x-services[.]xyz/`).

#### Vulnérabilités et vecteurs d'attaque
*   **Absence de CVE directe :** Le malware repose sur une conception logicielle malveillante plutôt que sur l'exploitation d'une faille logicielle connue.
*   **Abus de fonctionnalités légitimes :** Utilisation intensive des permissions Android (`QUERY_ALL_PACKAGES`) pour le ciblage et détournement de plateformes de commerce électronique pour masquer son infrastructure.
*   **Obfuscation :** L'utilisation d'un chargeur natif re-randomisé à chaque nouvelle compilation rend la détection statique par signature quasi impossible.

#### Recommandations
*   **Ne pas bloquer les hôtes légitimes :** Les plateformes comme *Basalam* ou *GitHub* utilisées comme "dead drops" ne doivent pas être bloquées, car elles sont des services légitimes. Il convient de se concentrer sur les indicateurs de comportement (ex: accès anormal aux champs biographiques ou exfiltration vers des domaines suspects).
*   **Analyse comportementale :** Surveiller les applications qui tentent de déchiffrer des métadonnées du manifeste ou qui effectuent des requêtes HTTP vers des profils utilisateurs publics.
*   **Détection des "Sinks" :** Porter une attention particulière aux composants du code responsables de la construction des URL et du déchiffrement des données (`X_ROUTES`, `X_BANKS`), plutôt que de se fier uniquement aux chaînes de caractères statiques.
*   **Hygiène mobile :** Sensibiliser les utilisateurs à ne télécharger des applications que depuis des sources officielles et à vérifier les permissions demandées (bien que Novinarya évite les permissions d'accessibilité, il demande des accès larges aux paquets installés).

---
[Source](https://starlabs.sg/blog/2026/10-novinarya-an-android-stealer-that-hides-its-live-c2-in-a-shop-bio/){:target="_blank"}
