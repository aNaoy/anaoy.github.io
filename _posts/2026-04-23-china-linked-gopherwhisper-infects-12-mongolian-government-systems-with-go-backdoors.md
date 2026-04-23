---
title: 'China-Linked GopherWhisper Infects 12 Mongolian Government Systems with Go Backdoors'
date: 2026-04-23
permalink: /posts/2026/04/23/china-linked-gopherwhisper-infects-12-mongolian-government-systems-with-go-backdoors/
tags:
- veille-cyber
- hackernews
---
### GopherWhisper : Une menace persistante liée à la Chine ciblant la Mongolie

Un nouveau groupe d'APT (Advanced Persistent Threat) baptisé **GopherWhisper** a été identifié, ciblant activement des institutions gouvernementales en Mongolie depuis au moins novembre 2023. Ce groupe se distingue par l'utilisation intensive d'outils développés en langage Go et par le détournement de services légitimes pour ses activités malveillantes.

**Points clés :**
* **Infrastructures ciblées :** Au moins 12 systèmes gouvernementaux mongols confirmés comme infectés, avec des preuves d'autres victimes potentielles via les serveurs de contrôle du groupe.
* **Méthodologie :** Le groupe utilise des injecteurs et des chargeurs pour déployer une panoplie de backdoors.
* **Exfiltration et C&C :** GopherWhisper détourne des services courants (Discord, Slack, Microsoft 365 Outlook, file.io) pour communiquer avec ses serveurs de commande et exfiltrer des données sensibles.
* **Attribution :** L'analyse des métadonnées (heures d'activité alignées sur l'heure normale de Chine et paramètres régionaux) confirme l'origine probable du groupe en Chine.

**Arsenal malveillant :**
Le groupe déploie une suite d'outils spécialisés :
* **Injecteurs/Chargeurs :** *JabGopher* et *FriendDelivery*.
* **Backdoors :**
    * *LaxGopher* (Go) : utilise Slack pour le C&C.
    * *RatGopher* (Go) : utilise Discord pour le C&C et le transfert de fichiers.
    * *BoxOfFriends* (Go) : exploite l'API Microsoft Graph via Outlook pour le C&C.
    * *SSLORDoor* (C++) : communique via des sockets bruts sur le port 443.
* **Outil d'exfiltration :** *CompactGopher* (Go) : collecte, compresse (ZIP) et chiffre (AES-CFB-128) des documents bureautiques (.docx, .pdf, .xls, etc.) avant de les exfiltrer via file.io.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, le groupe s'appuyant sur l'injection de DLL et l'exploitation de fonctionnalités légitimes de services tiers plutôt que sur l'exploitation directe de vulnérabilités logicielles connues.

**Recommandations :**
* **Surveillance réseau :** Bloquer ou surveiller étroitement les communications sortantes inhabituelles vers les plateformes de stockage cloud (file.io) et les services de collaboration (Discord, Slack) depuis les serveurs sensibles.
* **Inspection des processus :** Détecter les comportements suspects liés aux injecteurs (ex: *JabGopher*) et la présence de fichiers exécutables compilés en Go dans des répertoires non standards.
* **Gestion des identités :** Renforcer la sécurité des comptes Microsoft 365 en utilisant l'authentification multifacteur (MFA) pour prévenir l'abus de l'API Microsoft Graph.
* **Filtrage Egress :** Restreindre les communications via des sockets bruts sur le port 443 pour limiter l'efficacité des backdoors comme *SSLORDoor*.

---
[Source](https://thehackernews.com/2026/04/china-linked-gopherwhisper-infects-12.html){:target="_blank"}
