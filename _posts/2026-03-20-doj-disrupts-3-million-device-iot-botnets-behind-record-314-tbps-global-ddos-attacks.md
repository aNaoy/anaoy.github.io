---
title: 'DoJ Disrupts 3 Million-Device IoT Botnets Behind Record 31.4 Tbps Global DDoS Attacks'
date: 2026-03-20
permalink: /posts/2026/03/20/doj-disrupts-3-million-device-iot-botnets-behind-record-314-tbps-global-ddos-attacks/
tags:
- veille-cyber
- hackernews
---
### Démantèlement d'un réseau mondial de botnets IoT responsables d'attaques DDoS records

Le ministère de la Justice américain (DoJ), en collaboration avec des autorités internationales et des acteurs privés, a neutralisé l'infrastructure de commande et de contrôle (C2) de quatre botnets IoT majeurs : **AISURU, Kimwolf, JackSkid et Mossad**. Ces réseaux, ayant infecté environ 3 millions d'appareils (smart TV, caméras, routeurs, boîtiers Android), sont à l'origine d'attaques DDoS records atteignant jusqu'à 31,4 Tbps.

#### Points clés
*   **Méthodologie :** Les botnets utilisaient un modèle de « cybercriminalité à la demande » (cybercrime-as-a-service), exploitant des réseaux de proxys résidentiels pour infiltrer des appareils normalement protégés par des pare-feux domestiques.
*   **Impact :** Plus de 315 000 commandes d'attaques DDoS ont été émises, paralysant des infrastructures critiques et visant des cibles mondiales avec une puissance sans précédent.
*   **Enquête :** Les autorités ont identifié des suspects en Allemagne et au Canada (dont un jeune homme de 23 ans affirmant être victime d'usurpation d'identité). Aucune arrestation n'a encore été officiellement annoncée.

#### Vulnérabilités exploitées
*   **Vecteur principal :** Utilisation de réseaux de proxys résidentiels pour contourner les protections périmétriques.
*   **Faille spécifique :** Exposition du service **Android Debug Bridge (ADB)** sur des appareils Android (Smart TV, set-top boxes), permettant une prise de contrôle à distance non autorisée.

#### Recommandations de sécurité
*   **Désactivation d'ADB :** S'assurer que le mode « Débogage USB/Réseau » (Android Debug Bridge) est désactivé sur tous les appareils Android, particulièrement les TV et boîtiers multimédias connectés.
*   **Isolation réseau :** Segmenter le réseau domestique en isolant les objets connectés (IoT) sur un réseau Wi-Fi « Invité » pour limiter les risques de mouvement latéral vers les équipements sensibles.
*   **Mise à jour des firmwares :** Maintenir les routeurs, caméras et autres périphériques IoT à jour pour corriger les failles exploitées par les botnets.
*   **Sécurisation des accès :** Modifier systématiquement les mots de passe par défaut des équipements connectés.

---
[Source](https://thehackernews.com/2026/03/doj-disrupts-3-million-device-iot.html){:target="_blank"}
