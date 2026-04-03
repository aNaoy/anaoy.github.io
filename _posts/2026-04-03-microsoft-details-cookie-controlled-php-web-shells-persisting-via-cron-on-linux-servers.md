---
title: 'Microsoft Details Cookie-Controlled PHP Web Shells Persisting via Cron on Linux Servers'
date: 2026-04-03
permalink: /posts/2026/04/03/microsoft-details-cookie-controlled-php-web-shells-persisting-via-cron-on-linux-servers/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Les web shells PHP pilotés par cookies sur Linux

Des acteurs malveillants exploitent des web shells PHP sur des serveurs Linux en utilisant les cookies HTTP comme vecteur de commande. Cette technique permet d'exécuter du code à distance (RCE) tout en restant indétectable, car le code malveillant demeure dormant dans le trafic web légitime et ne s'active qu'en présence de valeurs de cookies spécifiques.

**Points clés :**
* **Dissimulation :** Les attaquants utilisent la superglobale `$_COOKIE` de PHP pour transmettre des instructions, évitant ainsi les paramètres URL ou les corps de requête suspects.
* **Persistance "Auto-réparatrice" :** Les assaillants configurent des tâches `cron` qui recréent périodiquement le script malveillant s'il est supprimé, assurant un accès constant.
* **Diversité des méthodes :** Les implémentations varient de simples marqueurs de déclenchement à des chargeurs PHP hautement obfusqués capables de reconstruire des fonctionnalités complexes à la volée.
* **Vecteur d'accès initial :** L'intrusion initiale s'effectue généralement via des identifiants compromis ou l'exploitation de vulnérabilités connues (CVE non spécifiée, dépend de l'environnement de l'hôte).

**Recommandations :**
* **Durcissement des accès :** Imposer l'authentification multifacteur (MFA) pour les accès SSH, les panneaux de contrôle d'hébergement et toutes les interfaces d'administration.
* **Audit et Surveillance :**
    * Inspecter régulièrement les tâches planifiées (`cron`) pour détecter des scripts de régénération suspects.
    * Surveiller les répertoires web pour identifier toute création ou modification inhabituelle de fichiers.
    * Analyser les logs à la recherche d'activités de connexion anormales.
* **Restrictions système :** Restreindre les capacités d'exécution des interpréteurs de shell via les panneaux de contrôle d'hébergement et limiter les privilèges des processus web.

---
[Source](https://thehackernews.com/2026/04/microsoft-details-cookie-controlled-php.html){:target="_blank"}
