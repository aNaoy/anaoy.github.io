---
title: 'New GopherWhisper APT group abuses Outlook, Slack, Discord for comms'
date: 2026-04-23
permalink: /posts/2026/04/23/new-gopherwhisper-apt-group-abuses-outlook-slack-discord-for-comms/
tags:
- veille-cyber
- bleepingcomp
---
### GopherWhisper : Nouveau groupe APT ciblant les infrastructures gouvernementales

Le groupe de menace persistante avancée (APT) « GopherWhisper », lié à la Chine et actif depuis 2023, utilise un arsenal sophistiqué basé principalement sur le langage Go pour cibler des entités gouvernementales, notamment en Mongolie. Les attaquants exploitent des services légitimes pour assurer leur communication de commande et de contrôle (C2) et exfiltrer des données sensibles.

**Points clés :**
* **Infrastructures de C2 détournées :** Les attaquants utilisent les API de Slack, Discord et Microsoft Graph (Outlook) pour piloter leurs malwares et échanger des commandes, rendant la détection réseau plus complexe.
* **Exfiltration :** Les données volées sont compressées via l'outil `CompactGopher` avant d'être envoyées vers le service de partage de fichiers *File.io*.
* **Attribution :** L'analyse des fuseaux horaires (UTC+8) et des métadonnées des serveurs de communication confirme une origine probable liée à des horaires de bureau en Chine.
* **Outils identifiés :** 
    * `LaxGopher` (Backdoor Go/Slack)
    * `RatGopher` (Backdoor Go/Discord)
    * `BoxOfFriends` (Backdoor Go/Outlook via Microsoft Graph)
    * `SSLORDoor` (Backdoor C++/OpenSSL sur port 443)
    * `JabGopher` et `FriendDelivery` (Injecteurs/Loaders)

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée dans le rapport, l'attaque reposant sur l'injection de bibliothèques malveillantes (`whisper.dll`) et le détournement d'APIs légitimes via des identifiants compromis ou hardcodés.

**Recommandations :**
* **Surveillance des flux :** Surveiller les communications anormales vers les API de services cloud (Slack, Discord, Microsoft Graph) provenant de processus inhabituels sur les postes de travail.
* **Utilisation des IoCs :** Appliquer les indicateurs de compromission (IoCs) fournis par ESET sur GitHub pour identifier les traces des malwares (ex: `svchost.exe` lançant des processus suspects ou injectant des DLL non signées).
* **Analyse comportementale :** Détecter l'exécution de binaires Go non autorisés et les activités de compression de données inhabituelles.
* **Gestion des identités :** Renforcer la sécurité des comptes connectés aux API cloud d'entreprise pour éviter le hardcodage d'identifiants dans des scripts malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/new-gopherwhisper-apt-group-abuses-outlook-slack-discord-for-comms/){:target="_blank"}
