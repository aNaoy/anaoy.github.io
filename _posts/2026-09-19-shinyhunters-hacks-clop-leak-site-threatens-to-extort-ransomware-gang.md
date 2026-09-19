---
title: 'ShinyHunters hacks Clop leak site, threatens to extort ransomware gang'
date: 2026-09-19
permalink: /posts/2026/09/19/shinyhunters-hacks-clop-leak-site-threatens-to-extort-ransomware-gang/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberguerre : Le groupe ShinyHunters pirate le site de fuite de données de Clop

Le groupe de cybercriminels ShinyHunters a compromis le site de fuite de données du collectif de rançongiciels Clop, marquant une escalade dans le conflit opposant les deux entités.

**Points clés :**
* **Compromission :** ShinyHunters a réussi à défigurer le site Tor de Clop, remplaçant son contenu par son propre logo.
* **Exfiltration de données :** Le groupe affirme avoir accédé aux logs système, au code source du site et aux clés privées de l'infrastructure Tor de Clop, ce qui leur permettrait potentiellement de contrôler l'adresse onion du site.
* **Objectif :** ShinyHunters prévoit d'extorquer le groupe Clop en représailles à des menaces physiques et verbales reçues précédemment, liées à une dispute sur l'exploitation d'une faille Oracle.
* **Origine du conflit :** Les tensions ont débuté en 2025 après que Clop aurait utilisé, sans autorisation, un exploit appartenant à ShinyHunters visant les serveurs Oracle E-Business Suite.

**Vulnérabilités exploitées :**
* La compromission initiale a été rendue possible par l'exploitation d'une faille de téléchargement de fichiers sans authentification au sein du CMS Grav (utilisé par le site de Clop).
* Le contexte mentionne également l'utilisation passée de la vulnérabilité **CVE-2025-61882** dans les serveurs Oracle E-Business Suite comme point de discorde entre les deux groupes.

**Recommandations :**
* **Sécurisation des CMS :** Maintenir les systèmes de gestion de contenu (CMS) à jour et désactiver toute fonction de téléchargement de fichiers non sécurisée.
* **Gestion des accès :** Appliquer le principe du moindre privilège sur les serveurs hébergeant des données sensibles pour limiter l'impact en cas de compromission (ex: accès restreint aux répertoires `/var/log`).
* **Protection des clés privées :** Utiliser des HSM (Hardware Security Modules) ou des coffres-forts numériques pour stocker les clés privées des services onion, afin d'éviter qu'elles ne soient exfiltrées en cas d'intrusion sur le serveur web.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-hacks-clop-leak-site-threatens-to-extort-ransomware-gang/){:target="_blank"}
