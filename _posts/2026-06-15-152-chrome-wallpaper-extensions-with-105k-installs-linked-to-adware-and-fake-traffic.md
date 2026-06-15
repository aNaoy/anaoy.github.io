---
title: '152 Chrome Wallpaper Extensions with 105K Installs Linked to Adware and Fake Traffic'
date: 2026-06-15
permalink: /posts/2026/06/15/152-chrome-wallpaper-extensions-with-105k-installs-linked-to-adware-and-fake-traffic/
tags:
- veille-cyber
- hackernews
---
### Réseau d'extensions Chrome malveillantes : Adware et fraude au trafic

Une campagne malveillante impliquant 152 extensions Google Chrome, se présentant comme des fonds d'écran dynamiques (live wallpapers), a été identifiée. Cumulant plus de 105 000 installations, ces extensions exploitent 38 comptes développeurs distincts pour diffuser des programmes potentiellement indésirables (PUP) et générer du trafic publicitaire frauduleux.

**Points clés :**
*   **Fraude au trafic :** Les extensions simulent artificiellement du trafic « organique » vers des sites tiers en ouvrant des onglets automatisés lors de l'installation et de la désinstallation. Elles utilisent des redirections masquées pour tromper les systèmes de mesure de Google et faire passer ces visites automatisées pour des clics humains légitimes.
*   **Collecte de données abusive :** Bien que les fiches du Chrome Web Store affirment ne pas collecter de données, les politiques de confidentialité révèlent le suivi des adresses IP, des fournisseurs d'accès, des clics et des sites référents, le tout partagé avec des réseaux publicitaires (Google AdSense, DoubleClick).
*   **Fonctionnalité cachée :** Le code JavaScript des extensions contient une capacité dormante permettant d'énumérer et de supprimer les bases de données IndexedDB locales.
*   **Origine :** L'opération, probablement motivée par des gains financiers, semble provenir de Turquie.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à cette campagne, car il s'agit d'une utilisation abusive des fonctionnalités légitimes des extensions Chrome (via `js/bg.js`) plutôt que de l'exploitation d'une faille technique spécifique.

**Recommandations :**
*   **Suppression immédiate :** Désinstallez toute extension liée à ces thèmes de fonds d'écran suspects.
*   **Vigilance sur les permissions :** Avant d'installer une extension, vérifiez systématiquement sa politique de confidentialité réelle plutôt que de se fier à la description du Store.
*   **Nettoyage des données :** Étant donné la capacité des extensions à manipuler les bases de données IndexedDB, il est conseillé de vider le cache et les données de navigation après la suppression des extensions douteuses.
*   **Réduction de la surface d'attaque :** Limitez l'installation d'extensions tierces, particulièrement celles proposant des fonctionnalités cosmétiques simples qui demandent des accès étendus au navigateur.

---
[Source](https://thehackernews.com/2026/06/152-chrome-wallpaper-extensions-with.html){:target="_blank"}
