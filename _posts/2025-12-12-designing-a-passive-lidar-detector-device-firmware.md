---
title: 'Designing a Passive LiDAR Detector Device - Firmware'
date: 2025-12-12
permalink: /posts/2025/12/12/designing-a-passive-lidar-detector-device-firmware/
tags:
- veille-cyber
- zerodaysfans
---
## Détection Passive de LiDAR : Développement du Firmware

Ce document détaille la conception et l'implémentation du firmware pour un appareil capable de détecter passivement les signaux LiDAR, notamment ceux émis par les appareils Apple TrueDepth. L'objectif est de distinguer le signal LiDAR d'autres sources de bruit ou de signaux parasites.

### Concepts Clés et Mesures

Le firmware repose sur plusieurs concepts pour analyser le signal lumineux reçu par des photodiodes :

*   **Détection de signaux discrets:** Il ne s'agit pas seulement de détecter une lumière, mais de différencier de multiples faisceaux lumineux discrets d'autres sources.
*   **Mesures multiples:** Plusieurs types de mesures sont effectuées pour caractériser le signal LiDAR :
    *   **Fréquence (Goertzel):** Recherche de la fréquence dominante (60Hz et ses harmoniques potentielles) du signal.
    *   **Fréquence de Répétition des Impulsions (PRF):** Analyse de la stabilité temporelle du signal, par opposition aux rafales intermittentes d'autres sources.
    *   **"Burstlikeness" (Tendance aux rafales):** Analyse de la distribution des magnitudes du signal pour évaluer sa stabilité.
    *   **Coïncidence Spatiale:** Détermination si certains, mais pas tous, les capteurs ont réagi simultanément, reflétant la nature en faisceaux du LiDAR.
    *   **Veto TSOP IR-Decode:** Utilisation d'un décodeur de signaux infrarouges (TSOP) pour exclure les signaux de télécommandes IR.
    *   **Clignotement Périodique:** Détection d'un cycle de service potentiellement détectable, bien que moins fiable en raison des mouvements.

### Méthodologie et Implémentation

Pour gérer ces mesures, le firmware utilise :

*   **Système de Pondération (Scoring):** Un système de points pondérés permet de décider si un signal est bien celui du LiDAR recherché. Les détections positives des caractéristiques recherchées ajoutent des points, tandis que les détections de signaux IR ajoutent des points négatifs.
*   **Bucketing (Échantillonnage):** Les événements de mesure sont regroupés dans des échantillons fixes de 4 ms appelés "Buckets".
*   **Tampons Circulaires (Ring Buffers):** Permettent une lecture et une écriture rapides des données de mesure pour ne pas gaspiller la capacité matérielle.
*   **Acquisition de Signal par Interruptions:** Utilisation des timers d'interruption du microcontrôleur SAMD21 pour une capture précise et rapide des signaux.
*   **Hystérésis (Latching):** Un mécanisme de comptage prévient les déclenchements ou désactivations intempestifs, assurant une indication de détection stable.

Les traitements logiciels incluent le **Detrending** (suppression du décalage DC), le **Hann Smoothing** (lissage de la forme d'onde) et l'algorithme de **Goertzel** pour l'analyse fréquentielle.

### Points Clés

*   **Détection de 60Hz et harmoniques:** La fréquence principale du signal LiDAR est une caractéristique clé.
*   **Distinction des rafales:** Les signaux stables sont préférés aux signaux "bursty".
*   **Analyse spatiale des faisceaux:** La façon dont les capteurs réagissent ensemble est un indicateur fort.
*   **Veto des télécommandes IR:** L'utilisation de bibliothèques existantes simplifie l'exclusion de ces signaux.
*   **Gestion des faux positifs:** Des mesures comme la fréquence, la coïncidence spatiale et le veto TSOP sont essentielles.
*   **Optimisation sur SAMD21:** L'utilisation d'interruptions et de tampons circulaires est cruciale pour les performances.
*   **Hystérésis pour la stabilité de l'indicateur:** Assure une indication de détection fiable.

### Vulnérabilités potentielles et Recommandations

Bien que l'article ne mentionne pas explicitement de vulnérabilités CVE dans le sens d'exploits de sécurité logicielle traditionnels, il aborde les défis liés aux **faux positifs**.

**Points faibles / Vulnérabilités potentielles (au sens de détection non fiable) :**

*   **Interférence de sources à 60Hz:** Les ampoules domestiques et certains téléviseurs peuvent générer des signaux à 60Hz ou 120Hz, nécessitant une discrimination fine.
*   **Signaux de télécommandes IR:** Ces signaux peuvent ressembler à des signaux LiDAR à première vue, d'où le besoin d'un "veto" spécifique.
*   **Variabilité du signal LiDAR:** Le "clignotement périodique" ou le mouvement de la source peuvent rendre la détection moins fiable dans certaines conditions.
*   **Bruit ambiant:** La détection doit être robuste face à divers types de bruits lumineux et infrarouges.

**Recommandations issues de l'article pour améliorer la fiabilité de la détection :**

*   **Combinaison de multiples mesures:** Ne pas se fier à une seule méthode, mais utiliser un système de pondération pour combiner les indices de différentes analyses (Fréquence, Spatiale, Burstlikeness).
*   **Réglage fin des seuils:** Les valeurs seuils (par exemple, `BURST_RATIO_NEED`, `FRE_DOM_RATIO`, `CV` pour le PRF) nécessitent un réglage précis pour optimiser le compromis entre détection correcte et faux positifs.
*   **Amélioration des algorithmes:** L'article mentionne que des améliorations sont possibles, notamment dans la détection du cycle de service ("Periodic Blink").
*   **Analyse des données historiques:** L'utilisation de "windows" glissants et de tampons circulaires permet de considérer un historique récent du signal.
*   **Veto ciblé:** Le mécanisme de veto basé sur le décodage de signaux IR est une recommandation forte pour éliminer une classe courante de faux positifs.

Il est mentionné que les améliorations futures pourraient concerner le choix des composants et le peaufinage du firmware. L'approche consiste à s'assurer que plusieurs indicateurs de fiabilité du signal LiDAR sont satisfaits simultanément pour déclencher une détection positive.

---
[Source](https://www.atredis.com/blog/2025/12/1/designing-a-passive-lidar-detector-device-firmware){:target="_blank"}
