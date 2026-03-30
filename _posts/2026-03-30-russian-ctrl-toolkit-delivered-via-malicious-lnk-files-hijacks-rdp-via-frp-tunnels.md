---
title: 'Russian CTRL Toolkit Delivered via Malicious LNK Files Hijacks RDP via FRP Tunnels'
date: 2026-03-30
permalink: /posts/2026/03/30/russian-ctrl-toolkit-delivered-via-malicious-lnk-files-hijacks-rdp-via-frp-tunnels/
tags:
- veille-cyber
- hackernews
---
### Analyse du toolkit malveillant CTRL : RDP Hijacking et tunnelisation FRP

Le toolkit « CTRL », d’origine russe, est une plateforme modulaire .NET conçue pour l'exfiltration de données et la prise de contrôle à distance. Contrairement aux RAT (Remote Access Trojans) classiques, ce malware privilégie une discrétion accrue en faisant transiter l'intégralité de son activité de commande et contrôle (C2) par des tunnels RDP.

**Points clés :**
*   **Vecteur d'infection :** Fichiers LNK malveillants déguisés en dossiers de clés privées.
*   **Architecture :** Utilisation d'un chargement en plusieurs étapes (décodage en mémoire) et communication via des *named pipes* Windows pour éviter les traces réseau suspectes.
*   **Mécanismes de persistance :** Tâches planifiées et création de comptes utilisateurs locaux en porte dérobée.
*   **Stratégie de discrétion :** Absence d'adresses C2 codées en dur. Tout le trafic passe par des tunnels FRP (*Fast Reverse Proxy*) encapsulés dans des sessions RDP.
*   **Capacités :** Keylogging, vol de codes PIN Windows via une interface de phishing imitant l'authentification native, et diffusion de fausses notifications de navigateur.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifique, mais l'attaque repose sur :
*   Le détournement de sessions RDP (via l'outil `RDPWrapper.exe` pour permettre des sessions concurrentes illimitées).
*   L'abus d'outils légitimes et de techniques d'ingénierie sociale (fichiers LNK, phishing UI).

**Recommandations de sécurité :**
*   **Sensibilisation :** Former les utilisateurs à la méfiance vis-à-vis des raccourcis (.lnk) non sollicités, même s'ils semblent être des dossiers.
*   **Gestion des accès :** Restreindre l'utilisation du RDP et surveiller les ouvertures de sessions RDP concurrentes suspectes.
*   **Filtrage et surveillance :**
    *   Bloquer ou surveiller les connexions sortantes vers des ports non standard utilisés par FRP.
    *   Surveiller la création de nouveaux comptes utilisateurs locaux et la modification des tâches planifiées.
    *   Utiliser des solutions EDR/XDR pour détecter l'exécution de commandes PowerShell masquées et l'injection de DLL en mémoire.
*   **Sécurité Windows :** Appliquer les bonnes pratiques de sécurité sur les terminaux, notamment en désactivant le chargement de scripts non signés et en limitant l'exécution de binaires dans les répertoires temporaires.

---
[Source](https://thehackernews.com/2026/03/russian-ctrl-toolkit-delivered-via.html){:target="_blank"}
