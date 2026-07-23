---
title: 'Chaos Ransomware Uses msaRAT to Route C2 Traffic Through Headless Chrome and Edge'
date: 2026-07-23
permalink: /posts/2026/07/23/chaos-ransomware-uses-msarat-to-route-c2-traffic-through-headless-chrome-and-edge/
tags:
- veille-cyber
- hackernews
---
### msaRAT : Le malware "Chaos" détourne les navigateurs pour son C2

Le groupe de ransomware Chaos utilise un implant Rust baptisé **msaRAT** pour établir un canal de commande et de contrôle (C2) furtif. Plutôt que de communiquer directement, le malware pilote les navigateurs Chrome ou Edge en mode "headless" (sans interface) via le protocole de débogage (CDP).

**Points clés :**
*   **Contournement des défenses :** Le malware injecte du JavaScript dans le navigateur pour faire transiter les données via un canal WebRTC relayé par le service TURN de Twilio.
*   **Furtivité réseau :** Les flux de données semblent provenir de connexions légitimes vers Cloudflare et Twilio, masquant totalement l'adresse réelle du serveur de l'attaquant.
*   **Double chiffrement :** Les communications sont protégées par le protocole DTLS du navigateur, encapsulant un second chiffrement interne (ChaCha-Poly1305).
*   **Vecteur d'attaque :** Le malware est déployé via un fichier MSI déguisé en mise à jour Windows, téléchargé par une commande `curl` simple.

**Vulnérabilités :**
*   Il n'existe aucune vulnérabilité logicielle spécifique (CVE) à patcher ; il s'agit d'un **détournement d'usage légitime** du protocole de débogage Chrome (CDP) et des services WebRTC.

**Recommandations :**
*   **Surveillance comportementale :** Détecter le lancement anormal de `chrome.exe` ou `msedge.exe` par des processus non interactifs (services, installateurs) avec les arguments `--headless=new` et `--remote-debugging-port`.
*   **Analyse des processus :** Corréler l'activité du navigateur avec des connexions loopback sur le port de débogage et des flux sortants WebRTC.
*   **Segmentation et inspection :** Bien que le blocage complet de Twilio ou Cloudflare soit complexe, la surveillance des comportements de navigation inhabituels reste le meilleur moyen de repérer l'activité de msaRAT.
*   **Sécurité des installateurs :** Restreindre l'exécution de fichiers MSI non signés ou provenant de sources inconnues et surveiller les téléchargements initiés par des utilitaires comme `curl` ou `powershell` dans des répertoires temporaires.

---
[Source](https://thehackernews.com/2026/07/chaos-ransomware-uses-msarat-to-route.html){:target="_blank"}
