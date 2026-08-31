---
title: 'Microsoft warns of TerminalFix attacks deploying reverse tunnels'
date: 2026-08-31
permalink: /posts/2026/08/31/microsoft-warns-of-terminalfix-attacks-deploying-reverse-tunnels/
tags:
- veille-cyber
- bleepingcomp
---
### TerminalFix : Une menace sophistiquée par tunnel inverse

La campagne **TerminalFix** détourne la technique « ClickFix » en utilisant de faux CAPTCHA Cloudflare pour inciter les utilisateurs à exécuter des commandes PowerShell malveillantes via Windows Terminal. Contrairement aux voleurs d'informations classiques, cette attaque établit un accès persistant permettant une intrusion profonde dans le réseau interne.

**Points clés :**
* **Chaîne d'infection multi-étapes :** Téléchargement d'un exécutable signé légitime couplé à une DLL malveillante.
* **Stéganographie :** Utilisation d'images PNG pour dissimuler des fragments de code, réassemblés en mémoire sur la machine cible.
* **Tunnel inverse :** Déploiement d'un module Python via WebSockets (vers `gitnow[.]dev:443`) permettant un proxy TCP arbitraire (SOCKS5).
* **Objectifs :** Reconnaissance réseau (Active Directory, contrôleurs de domaine), exfiltration de données, mouvement latéral et déploiement potentiel de ransomwares.
* **Persistance :** Mise en place de tâches planifiées et de clés de registre exécutées toutes les heures.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'ingénierie sociale (tromper l'utilisateur pour qu'il exécute manuellement des scripts dans PowerShell).

**Recommandations :**
* **Contrôle et surveillance :** Restreindre et journaliser strictement l'exécution de PowerShell.
* **Détection :** Surveiller toute activité suspecte du processus `LockScreenContentServer.exe` en dehors de son chemin d'installation légitime.
* **Durcissement :** Renforcer les configurations des navigateurs et des solutions de protection des points de terminaison (EDR/EPP).
* **Réponse à incident :** En cas de compromission, isoler la machine, rechercher des signes de mouvement latéral et procéder à une réinitialisation immédiate des identifiants (particulièrement ceux à privilèges élevés).

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-warns-of-terminalfix-attacks-deploying-reverse-tunnels/){:target="_blank"}
