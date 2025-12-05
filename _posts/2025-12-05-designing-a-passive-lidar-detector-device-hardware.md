---
title: 'Designing a Passive LiDAR Detector Device - Hardware'
date: 2025-12-05
permalink: /posts/2025/12/05/designing-a-passive-lidar-detector-device-hardware/
tags:
- veille-cyber
- zerodaysfans
---
**Détection Passive du LiDAR des Smartphones**

La technologie LiDAR embarquée dans certains smartphones, notamment les iPhones Pro, peut être détectée passivement. Ce système, utilisé notamment pour la reconnaissance faciale et la cartographie, émet un motif de points infrarouges à une fréquence spécifique (60 Hz). Il est activé par défaut dès l'ouverture de l'application appareil photo, avant même la prise de vue.

**Points Clés :**

*   **Principe de fonctionnement :** Le système LiDAR des iPhones Pro utilise un laser infrarouge (VCSEL) émettant à 940 nm, projetant un motif de points à 60 Hz. Ce signal peut être observé avec des caméras dépourvues de filtre infrarouge.
*   **Détection précoce :** La détection de l'activation du LiDAR permet de savoir que l'application appareil photo est ouverte sur un appareil ciblé, même avant qu'une photo ne soit prise.
*   **Composants clés pour la détection :** La conception d'un appareil de détection nécessite de pouvoir :
    *   Percevoir le signal infrarouge sous forme de faisceaux lumineux.
    *   Convertir la lumière en signal analogique.
    *   Numériser ce signal.
    *   Analyser des caractéristiques comme la fréquence, la répétition des impulsions, et la simultanéité de la détection par plusieurs capteurs.
*   **Choix des composants :** Des photodiodes optimisées pour la longueur d'onde de 940 nm sont recommandées pour une détection nette. L'utilisation de filtres passe-bande est également cruciale pour distinguer le signal LiDAR des émissions lumineuses ambiantes (écrans, etc.). Des composants rapides comme les amplificateurs opérationnels 10 MHz ou les triggers de Schmitt, associés à un microcontrôleur performant et économe en énergie (comme le SAMD21), sont nécessaires pour le traitement du signal.
*   **Conception matérielle :** La conception privilégiée utilise des triggers de Schmitt et implique plusieurs capteurs infrarouges discrets. La disposition de ces capteurs est pensée pour pouvoir différencier le motif de points du LiDAR d'autres sources d'interférences, en analysant si certains capteurs seulement détectent le signal.

**Vulnérabilités :**

*   Bien qu'aucune vulnérabilité CVE spécifique ne soit mentionnée dans cet article, la capacité de détecter l'activation du LiDAR peut potentiellement révéler des informations sur l'utilisation d'un appareil à distance. Par exemple, savoir qu'un appareil a l'application appareil photo ouverte peut indiquer une intention de photographier ou d'enregistrer.

**Recommandations :**

*   Les appareils équipés de cette technologie devraient être conscients que leur activité de scan LiDAR est potentiellement détectable par des dispositifs externes.
*   Pour les développeurs d'appareils de détection, il est recommandé d'utiliser des photodiodes de 940 nm et des filtres passe-bande, ainsi qu'une architecture matérielle capable de traiter les signaux à haute fréquence et de corréler les mesures de plusieurs capteurs.

---
[Source](https://www.atredis.com/blog/2025/11/20/designing-a-passive-lidar-detection-sensor){:target="_blank"}
