---
title: 'Armored Likho digging a snake pit: inside the covert BusySnake Stealer campaign'
date: 2026-07-03
permalink: /posts/2026/07/03/armored-likho-digging-a-snake-pit-inside-the-covert-busysnake-stealer-campaign/
tags:
- veille-cyber
- securelist
---
### Analyse de la campagne BusySnake Stealer par le groupe Armored Likho

Le groupe APT « Armored Likho » (aussi appelé Eagle Werewolf) mène actuellement une campagne d'espionnage informatique et de vol de données ciblant des agences gouvernementales et le secteur de l'énergie en Russie, au Brésil et au Kazakhstan. Les attaquants utilisent des outils modulaires sophistiqués, souvent générés par IA, pour contourner les analyses dynamiques.

**Points clés :**
*   **Vecteur d'infection :** Spear-phishing utilisant des archives (ZIP/RAR) contenant des exécutables NSIS ou des raccourcis LNK piégés.
*   **BusySnake Stealer :** Un infostealer Python 3.12, hautement modulaire, protégé par PyArmor, capable de voler des mots de passe, des cookies, des portefeuilles crypto et des données Telegram.
*   **Fonctionnalités avancées :** Intégration d'un tunnel SSH inverse pour un accès distant persistant, exfiltration de captures d'écran et exécution de scripts Python en mémoire pour éviter toute détection sur disque.
*   **Évolution :** Les versions récentes utilisent des objets COM pour la persistance et un framework de gestion de tâches dynamique pour communiquer avec le serveur C2.

**Vulnérabilités exploitées :**
*   **ZDI-CAN-25373 :** Une vulnérabilité dans les fichiers LNK de Windows permettant de masquer des paramètres d'exécution malveillants via des caractères spéciaux.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs aux risques liés aux pièces jointes provenant de courriels non sollicités, particulièrement celles mimant des documents administratifs ou des tests psychologiques.
*   **Filtrage réseau :** Bloquer les communications vers les domaines et adresses IP associés aux serveurs de commande et de contrôle (C2).
*   **Durcissement des postes :** 
    *   Surveiller les processus suspects tels que `powershell.exe` ou `rundll32.exe` initiés par des fichiers LNK.
    *   Restreindre l'exécution de scripts Python et l'installation de bibliothèques tierces (pip) non autorisées sur les postes critiques.
    *   Désactiver ou auditer les associations de fichiers LNK pour limiter les risques liés à l'exploitation des raccourcis Windows.
*   **Sécurité des navigateurs :** Appliquer des politiques de groupe (GPO) interdisant l'installation d'extensions non approuvées et renforcer la protection des bases de données de mots de passe locales (ex: éviter les politiques de stockage par défaut sans mot de passe maître sur Firefox).

---
[Source](https://securelist.com/tr/armored-likho-apt-with-busysnake-stealer/120292/){:target="_blank"}
