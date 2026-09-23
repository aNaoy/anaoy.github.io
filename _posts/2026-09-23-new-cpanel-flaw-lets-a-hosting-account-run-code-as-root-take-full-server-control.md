---
title: 'New cPanel Flaw Lets a Hosting Account Run Code as Root, Take Full Server Control'
date: 2026-09-23
permalink: /posts/2026/09/23/new-cpanel-flaw-lets-a-hosting-account-run-code-as-root-take-full-server-control/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans cPanel et WP Toolkit

Trois vulnérabilités majeures ont été identifiées dans cPanel & WHM ainsi que dans le plugin WP Toolkit, permettant potentiellement à un utilisateur disposant d'un simple compte d'hébergement de compromettre l'intégralité d'un serveur.

**Points clés :**
*   **Escalade de privilèges (Root) :** La faille la plus critique permet à un utilisateur authentifié d'exécuter du code avec des privilèges root.
*   **Altération de bases de données :** Une vulnérabilité dans WP Toolkit permet à un utilisateur de modifier les bases de données appartenant à d'autres comptes sur le même serveur.
*   **Fuite de données :** Une faille de sécurité permet de consulter les événements de calendrier et les contacts d'autres utilisateurs.

**Vulnérabilités identifiées :**
*   **CVE-2026-87899 :** Exécution de code à distance en tant que root via les services CalDAV/CardDAV.
*   **CVE-2026-87900 :** Manipulation non autorisée de bases de données tierces via WP Toolkit.
*   **CVE-2026-68490 :** Lecture non autorisée d'informations personnelles (calendriers/contacts) par un utilisateur local.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par cPanel sans délai.
    *   **Pour cPanel & WHM :** Mettre à jour vers les versions 11.134.0.57, 11.136.0.41, 11.138.0.8 ou supérieure via l'interface WHM ou la commande `/usr/local/cpanel/scripts/upcp --force`.
    *   **Pour WP Toolkit :** Installer manuellement la version 6.11.3 ou supérieure à l'aide du script d'installation fourni par l'éditeur.
*   **Aucun contournement temporaire :** L'éditeur n'a fourni aucune solution palliative ; la mise à jour logicielle est la seule méthode sécurisée pour protéger le serveur.

---
[Source](https://thehackernews.com/2026/09/new-cpanel-flaw-lets-hosting-account_0272795595.html){:target="_blank"}
