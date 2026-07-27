---
title: 'Java Spring Boot "heapdump" scans, (Mon, Jul 27th)'
date: 2026-07-27
permalink: /posts/2026/07/27/java-spring-boot-heapdump-scans-mon-jul-27th/
tags:
- veille-cyber
- sans-isc
---
### Risques liés à l'exposition des dumps de mémoire dans Spring Boot

L'exposition non sécurisée de l'endpoint `/actuator/heapdump` dans les applications Java Spring Boot constitue une faille critique. Ce fichier (`heapdump.hprof`) contient une image mémoire complète de l'application, incluant des données hautement sensibles telles que des clés d'API, des mots de passe de bases de données et des identifiants de connexion aux systèmes backend.

**Points clés**
* **Fonctionnalité détournée :** L'endpoint est conçu pour le débogage, mais son accès public permet aux attaquants de récolter des secrets en clair.
* **Vecteur d'attaque :** Les attaquants ciblent les chemins configurés (ex: `/admin-api/actuator/heapdump`) en utilisant des combinaisons d'identifiants par défaut (ex: `admin:admin`) pour contourner les protections.
* **Visibilité :** La présence de ces fichiers dans des environnements de production est souvent due à une mauvaise configuration de la sécurité ou à l'utilisation de paramètres par défaut.

**Vulnérabilités**
Bien qu'il s'agisse principalement d'un problème de configuration (misconfiguration), cette exposition est souvent répertoriée dans le cadre de vulnérabilités d'accès non autorisé aux endpoints d'administration (souvent associées à des failles de type **CWE-200** : *Exposure of Sensitive Information to an Unauthorized Actor*).

**Recommandations**
* **Sécurisation via Spring Security :** Restreindre strictement l'accès aux endpoints de gestion (`/actuator/**`) en exigeant une authentification forte et des privilèges administratifs.
* **Désactivation par défaut :** Désactiver les endpoints inutiles en production dans le fichier `application.yml` : `management.endpoint.heapdump.enabled=false`.
* **Modification du chemin :** Éviter les chemins standards (`/actuator`) et utiliser des préfixes personnalisés complexes pour limiter les attaques par force brute ou par scan automatique.
* **Gestion des accès réseau :** Isoler les endpoints d'administration afin qu'ils ne soient accessibles que depuis des réseaux internes sécurisés (VPN ou IP whitelist) et non depuis Internet.

---
[Source](https://isc.sans.edu/diary/rss/33188){:target="_blank"}
