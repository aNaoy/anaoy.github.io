---
title: 'Increasing Searches for ZIP Files, (Thu, Aug 28th)'
date: 2025-08-28
permalink: /posts/2025/08/28/increasing-searches-for-zip-files-thu-aug-28th/
tags:
- veille-cyber
- sans-isc
---
### Augmentation des tentatives d'accès aux fichiers ZIP

Les journaux d'un honeypot web révèlent une augmentation significative des requêtes de fichiers ZIP au cours de la dernière année. Ces requêtes ciblent des noms de fichiers courants comme `backup.zip`, `web.zip`, `www.zip`, etc., suggérant une recherche de sauvegardes ou de fichiers de configuration potentiellement exposés.

**Points clés :**

*   L'activité observée n'est pas liée à une vulnérabilité spécifique du logiciel ZIP lui-même.
*   Les noms de fichiers demandés correspondent souvent à des noms que des administrateurs système ou des développeurs pourraient utiliser pour des sauvegardes temporaires ou des archives.
*   La liste des noms de fichiers ZIP ciblés s'allonge, incluant désormais des noms plus spécifiques comme `env.production.zip`, `cloud-config.zip`, `ssh_keys.zip`.

**Vulnérabilités potentielles exploitées (implicites) :**

L'exposition de tels fichiers sur un serveur web constitue une faiblesse. Si ces fichiers ZIP contiennent des informations sensibles (identifiants, clés privées, données de configuration, code source), leur accès non autorisé peut mener à de graves compromissions. Bien que l'article ne mentionne pas de CVE spécifiques, l'exposition de sauvegardes de sites web ou de fichiers de configuration est une pratique dangereuse.

**Recommandations :**

*   **Restreindre le téléchargement de fichiers ZIP :** Si possible, configurer le serveur web pour empêcher le téléchargement direct de fichiers avec l'extension `.zip`.
*   **Surveiller le répertoire racine du document :** Mettre en place une surveillance pour détecter la présence de fichiers ZIP non autorisés ou inattendus dans les répertoires accessibles via le web.
*   **Renforcer le contrôle des changements :** Appliquer des processus stricts de gestion des changements pour s'assurer que les fichiers de sauvegarde ou de configuration ne soient pas accidentellement ou intentionnellement laissés en accès libre sur les serveurs web par les administrateurs ou les développeurs.

---
[Source](https://isc.sans.edu/diary/rss/32242){:target="_blank"}
