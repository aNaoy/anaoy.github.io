---
title: 'Scans for "adminer", (Wed, Mar 18th)'
date: 2026-03-19
permalink: /posts/2026/03/19/scans-for-adminer-wed-mar-18th/
tags:
- veille-cyber
- sans-isc
---
### La montée des scans ciblant Adminer

L’outil de gestion de base de données **Adminer** fait face à une recrudescence significative des scans automatisés par des attaquants. Bien que réputé pour sa simplicité et sa sécurité supérieure par rapport à son prédécesseur phpMyAdmin, sa popularité croissante en fait une cible privilégiée.

**Points clés :**
* **Fonctionnement minimaliste :** Adminer ne stocke pas de configurations d'accès ; il repose sur l'authentification directe auprès de la base de données, évitant ainsi le risque de fuite de fichiers de secrets.
* **Méthodes d'attaque :** Les attaquants recherchent activement des fichiers spécifiques nommés selon le format `adminer-[version]-[type]-[lang].php`.
* **Vulnérabilités :** Le système est vulnérable aux attaques par force brute. Bien qu'une limite de 30 tentatives par 30 minutes soit instaurée, l'absence native de double authentification (2FA) constitue une faiblesse majeure pour les utilisateurs ayant des mots de passe faibles.

**Vulnérabilités :**
* Risque de force brute sur les identifiants de base de données.
* Absence de MFA native (nécessite l'ajout de plugins tiers).
* Aucune CVE spécifique mentionnée dans l'article, le risque étant lié à l'exposition directe du service sur Internet.

**Recommandations :**
* **Ne jamais exposer Adminer directement sur Internet.**
* Appliquer les conseils de sécurité fournis par les développeurs d'Adminer.
* Utiliser des plugins de sécurité dédiés pour implémenter la double authentification (OTP).
* Maintenir le fichier Adminer à jour et protéger son accès par des mesures réseau (VPN, filtrage IP, authentification au niveau du serveur Web).

---
[Source](https://isc.sans.edu/diary/rss/32808){:target="_blank"}
