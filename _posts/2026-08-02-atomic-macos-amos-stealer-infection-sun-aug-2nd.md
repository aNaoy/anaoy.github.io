---
title: 'Atomic MacOS (AMOS) stealer infection, (Sun, Aug 2nd)'
date: 2026-08-02
permalink: /posts/2026/08/02/atomic-macos-amos-stealer-infection-sun-aug-2nd/
tags:
- veille-cyber
- sans-isc
---
### Analyse de l'infection par le malware Atomic MacOS (AMOS)

Cette étude détaille le fonctionnement d'une campagne de distribution du stealer **Atomic MacOS (AMOS)**. Le vecteur d'attaque repose sur l'ingénierie sociale : via une page web malveillante (ex: `getmacouscloud[.]com`), les victimes sont incitées à copier et exécuter une commande dans le Terminal macOS sous prétexte d'installer un "kit d'outils" système. Cette commande télécharge et exécute silencieusement le malware, qui exfiltre ensuite des données sensibles.

#### Points clés
*   **Vecteur :** Exécution manuelle de scripts shell via le Terminal (copier-coller).
*   **Comportement :** Le malware s'installe de manière persistante dans les répertoires système cachés (`/Library/Application Support/`).
*   **Exfiltration :** Le stealer cible spécifiquement les informations d'identification, les données de messagerie, les portefeuilles de cryptomonnaies et les fichiers locaux.
*   **C2 (Commande et Contrôle) :** Le malware communique via des requêtes HTTP (port 80) vers une infrastructure distante (ex: `188.166.78.138`) pour exfiltrer les données collectées et recevoir des tâches.

#### Vulnérabilités exploitées
*   **Vulnérabilité humaine :** L'attaque ne repose pas sur une faille logicielle spécifique (CVE), mais sur l'exploitation de la confiance de l'utilisateur pour contourner les protections natives du système via l'exécution de commandes privilégiées dans le Terminal.

#### Recommandations de sécurité
*   **Sensibilisation :** Ne jamais copier-coller de commandes provenant de sites web inconnus dans un Terminal, particulièrement celles demandant une élévation de privilèges (mot de passe utilisateur).
*   **Filtrage réseau :** Bloquer les connexions sortantes vers les domaines et adresses IP suspects identifiés (ex: `getmacouscloud[.]com`, `render65[.]com`, et `188.166.78.138`).
*   **Monitoring :** Surveiller l'exécution de scripts (`zsh`, `bash`) suspects dans le répertoire `/tmp` et vérifier la persistance anormale dans les répertoires `~/Library/Application Support/`.
*   **Antivirus/EDR :** Maintenir les solutions de sécurité à jour pour détecter les signatures des binaires Mach-O identifiés (SHA-256 : `9f25ec...`, `0a03cf...`, `01a0d5...`).

---
[Source](https://isc.sans.edu/diary/rss/33208){:target="_blank"}
