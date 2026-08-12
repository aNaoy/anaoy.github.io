---
title: 'Sandworm hackers target IT pros with trojanized WireGuard VPN client'
date: 2026-08-12
permalink: /posts/2026/08/12/sandworm-hackers-target-it-pros-with-trojanized-wireguard-vpn-client/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'ingénierie sociale de Sandworm ciblant les professionnels de l'IT

Le groupe de menace russe Sandworm (APT44/UAC-0145) mène une campagne sophistiquée d'ingénierie sociale visant les administrateurs système et les professionnels de l'informatique. En usurpant l'identité d'entreprises légitimes, les attaquants piègent leurs victimes lors de faux processus de recrutement pour les inciter à installer un client VPN piégé.

**Points clés :**
* **Mode opératoire :** Les attaquants identifient des candidats sur des sites d'emploi, les contactent, puis les dirigent vers Telegram pour des entretiens vidéo sur Zoom.
* **Le piège :** Il est demandé aux candidats d'effectuer un test technique nécessitant l'installation d'un client VPN spécifique (« SopraVPN »), hébergé sur SourceForge et promu via de faux domaines d'entreprise.
* **Mécanisme malveillant :** Le client WireGuard modifié contient une option de configuration « SymmetricKey » non standard qui déchiffre et exécute du code PowerShell malveillant.
* **Technique d'évasion :** Le logiciel malveillant utilise un alphabet Base64 personnalisé et dynamique pour masquer ses chaînes de caractères et entraver l'analyse statique.
* **Charge utile :**
    * **Windows :** Création de tâches planifiées pour télécharger des charges utiles additionnelles.
    * **Linux :** Utilisation de cURL pour récupérer des exécutables depuis l'infrastructure des attaquants.

**Vulnérabilités :**
Aucune CVE spécifique n'est exploitée ; l'attaque repose sur l'installation volontaire d'un logiciel malveillant (trojan) par l'utilisateur final.

**Recommandations :**
* **Contrôle des accès :** Restreindre l'accès aux ressources de l'entreprise aux seuls appareils gérés et surveillés en permanence.
* **Sécurité des terminaux :** Déployer des solutions EDR (Endpoint Detection and Response) sur tous les postes, y compris les équipements personnels utilisés pour le travail.
* **Vigilance humaine :** Sensibiliser les employés aux risques liés aux processus de recrutement suspects, notamment les demandes d'installation de logiciels tiers ou de configuration VPN imposées en dehors des outils officiels.
* **Vérification :** Mener des enquêtes approfondies sur les domaines et les fichiers fournis dans le cadre de recrutements externes.

---
[Source](https://www.bleepingcomputer.com/news/security/sandworm-hackers-target-it-pros-with-trojanized-wireguard-vpn-client/){:target="_blank"}
