---
title: 'Attackers Heat French Supermarket Fridges Up to 50°C by Hijacking Danfoss Controllers'
date: 2026-10-13
permalink: /posts/2026/10/13/attackers-heat-french-supermarket-fridges-up-to-50c-by-hijacking-danfoss-controllers/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque massive contre les systèmes de réfrigération en France

Des centaines de supermarchés français (Intermarché, Carrefour, Monoprix, etc.) ont été victimes d'une cyberattaque visant les contrôleurs de réfrigération de la marque Danfoss. Les attaquants ont pris le contrôle distant de ces équipements pour activer le mode dégivrage et augmenter la température jusqu'à 50°C, entraînant des pertes alimentaires massives et des risques d'incendie.

**Points clés**
*   **Cibles :** Les contrôleurs de séries AK-SM et AK-SC, largement utilisés dans la grande distribution.
*   **Impact :** Des centaines de magasins touchés à travers la France, avec des répercussions signalées également dans plusieurs pays européens (Espagne, Belgique, Allemagne, etc.).
*   **Méthode :** L'attaque exploite l'exposition directe des interfaces de gestion des contrôleurs sur Internet, permettant un accès sans authentification sécurisée.
*   **Obsolescence :** Une grande partie des appareils compromis sont des modèles anciens (AK-SM 800, AK-SC 355) qui ne reçoivent plus de mises à jour de sécurité.

**Vulnérabilités identifiées (modèles récents)**
Bien qu'aucun lien direct n'ait été officiellement confirmé avec l'attaque actuelle, des vulnérabilités critiques ont été découvertes en 2025 sur le modèle récent AK-SM 800A :
*   **CVE-2025-41450 :** Contournement de l'authentification.
*   **CVE-2025-41451 :** Injection de commande (exécution de code à distance).
*   **CVE-2025-41452 :** Déni de service (DoS).

**Recommandations de sécurité (CERT-FR & Danfoss)**
*   **Isolation immédiate :** Déconnecter impérativement les contrôleurs de l'accès public à Internet. Si l'accès distant est indispensable, utiliser un VPN ou restreindre strictement l'accès à des adresses IP de confiance via un pare-feu.
*   **Mise à jour :** Appliquer les correctifs de firmware les plus récents pour les modèles pris en charge (AK-SM 800A).
*   **Durcissement :** En cas de compromission avérée ou par mesure préventive : effectuer une réinitialisation d'usine, modifier tous les mots de passe par défaut, vérifier les comptes utilisateurs et reconfigurer entièrement l'appareil.
*   **Obsolescence :** Remplacer les contrôleurs en fin de vie (AK-SM 800 et AK-SC 355) qui ne bénéficient plus de correctifs de sécurité.

---
[Source](https://thehackernews.com/2026/10/attackers-heat-french-supermarket.html){:target="_blank"}
