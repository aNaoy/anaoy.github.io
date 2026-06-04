---
title: 'Hackers Spied on a Stock Exchange Executives Outlook Mailbox for Five Months'
date: 2026-06-04
permalink: /posts/2026/06/04/hackers-spied-on-a-stock-exchange-executives-outlook-mailbox-for-five-months/
tags:
- veille-cyber
- hackernews
---
### Espionnage prolongé d'une boîte mail de haut dirigeant boursier

Une campagne d'espionnage sophistiquée a permis à des attaquants d'infiltrer la boîte Outlook d'un dirigeant d'une bourse mondiale pendant cinq mois (d'octobre 2025 à mars 2026). L'objectif était le vol d'informations stratégiques et confidentielles, sans recherche de gain financier immédiat.

**Points clés :**
*   **Tactique de furtivité :** Les attaquants ont exfiltré les e-mails par petits lots réguliers via Dropbox et OneDrive, en utilisant des connexions directes par adresse IP pour éviter les requêtes DNS suspectes.
*   **Masquage :** Des tâches planifiées se faisaient passer pour des services légitimes (Adobe, Lenovo, OneDrive).
*   **Outils utilisés :** Un outil personnalisé basé sur la bibliothèque *Aspose* pour convertir les fichiers OST/PST, ainsi que des outils reconnus comme *FRPC* (tunneling), *Secretsdump* (vol de credentials) et *SharpDecryptPwd*.
*   **Vecteur initial :** Inconnu, mais probablement lié à un mouvement latéral depuis un appareil précédemment compromis.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cette attaque. Il s'agit d'une intrusion utilisant des outils légitimes détournés ("Living off the Land") et non l'exploitation d'une faille logicielle spécifique.

**Recommandations :**
*   **Surveillance comportementale :** Surveiller étroitement les activités d'exportation de boîtes mail et les accès inhabituels à Outlook.
*   **Détection des flux :** Bloquer ou surveiller les téléchargements massifs vers des comptes Dropbox ou OneDrive personnels depuis le réseau de l'entreprise.
*   **Sécurité des privilèges :** Porter une attention particulière aux tentatives de dumping de credentials (Secretsdump) et aux contournements de l'UAC (User Account Control) sur les postes des utilisateurs disposant de privilèges élevés.
*   **Analyse réseau :** Rechercher les signes de tunneling (ex: FRPC) et les connexions vers des services cloud contournant les résolutions DNS habituelles.

---
[Source](https://thehackernews.com/2026/06/hackers-spied-on-stock-exchange.html){:target="_blank"}
