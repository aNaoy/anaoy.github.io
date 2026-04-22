---
title: '&#x5b;Guest Diary&#x5d; Beyond Cryptojacking: Telegram tdata as a Credential Harvesting Vector, Lessons from a Honeypot Incident, (Wed, Apr 22nd)'
date: 2026-04-22
permalink: /posts/2026/04/22/x5bguest-diaryx5d-beyond-cryptojacking-telegram-tdata-as-a-credential-harvesting-vector-lessons-from-a-honeypot-incident-wed-apr-22nd/
tags:
- veille-cyber
- sans-isc
---
### Au-delà du minage : Le dossier « tdata » de Telegram comme vecteur de vol d'identité

Les cyberattaques modernes évoluent : le minage de cryptomonnaies sert désormais de simple reconnaissance pour préparer le vol de données sensibles. L'analyse d'un *honeypot* a révélé des attaquants ciblant spécifiquement le dossier `tdata` de Telegram Desktop afin de détourner des sessions utilisateurs de manière persistante, contournant ainsi l'authentification à deux facteurs (2FA).

**Points clés :**
*   **Vol de session :** Le dossier `tdata` contient les jetons d'authentification. En le copiant, un attaquant peut usurper l'identité d'une victime sur sa propre machine sans avoir besoin de ses identifiants ni du code 2FA.
*   **Méthodologie :** Après un accès initial (souvent via SSH), les attaquants scannent le système pour identifier des ressources (CPU) et localiser le répertoire `tdata` et les périphériques modem (visant à intercepter des SMS).
*   **Risque de persistance :** Contrairement au minage qui est éphémère, le vol de session permet un accès durable et une exploitation à long terme des comptes compromis.

**Vulnérabilités :**
*   **Accès SSH faible :** Utilisation de mots de passe vulnérables permettant l'accès initial (MITRE ATT&CK [T1110/001]).
*   **Exposition locale :** La structure de stockage de Telegram Desktop n'est pas chiffrée de manière à empêcher une copie simple du dossier de session par un utilisateur ou un processus malveillant ayant des droits sur le système.

**Recommandations :**
*   **Renforcement SSH :** Désactiver l'authentification par mot de passe au profit des clés SSH.
*   **Surveillance des fichiers :** Mettre en place un outil de surveillance de l'intégrité des fichiers (FIM) sur le dossier `tdata`. Toute lecture ou copie par un processus autre que Telegram doit déclencher une alerte immédiate.
*   **Gestion des sessions :** Auditer régulièrement les sessions actives dans les paramètres de Telegram et déconnecter tout appareil non reconnu.
*   **Détection comportementale :** Surveiller les commandes de recherche système (ex: `grep 'miner'`, `ls` sur `tdata`, énumération des périphériques `/dev/ttyGSM*`), qui sont des indicateurs précoces d'une intrusion.
*   **Prioriser le mobile :** Utiliser Telegram sur mobile (iOS/Android) limite le risque d'exfiltration de fichiers de session grâce au cloisonnement du système d'exploitation et à l'authentification biométrique.

---
[Source](https://isc.sans.edu/diary/rss/32888){:target="_blank"}
