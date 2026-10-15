---
title: 'Panchans Mining Island &#x5b;Guest Diary&#x5d;, (Wed, Oct 14th)'
date: 2026-10-15
permalink: /posts/2026/10/15/panchans-mining-island-x5bguest-diaryx5d-wed-oct-14th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du ver Panchan : Menace persistante de cryptominage

Le ver Panchan est un botnet P2P écrit en Go, actif depuis 2022. Conçu pour le minage de cryptomonnaies, il se distingue par sa persistance via l'utilisation de rootkits et sa capacité à se propager latéralement en volant des clés SSH sur les systèmes infectés.

**Points clés :**
* **Fonctionnement :** Utilise des techniques de mouvement latéral en exploitant le fichier `known_hosts` des utilisateurs compromis.
* **Command & Control (C2) :** Utilise des canaux Discord pour piloter les bots.
* **Indicateurs de compromission (IoC) :** Tentatives répétées de connexion SSH, consommation anormale de ressources système, processus impossibles à arrêter, présence de répertoires cachés au nom aléatoire (haute entropie) dans `/tmp` ou le répertoire utilisateur, et trafic réseau récurrent vers Discord.

**Vulnérabilités exploitées :**
* Bien qu'aucune CVE spécifique ne soit citée, l'infection repose sur une mauvaise configuration des services exposés : accès SSH public non sécurisé, utilisation de mots de passe faibles ou gestion laxiste des clés SSH (privilèges excessifs, absence d'expiration).

**Recommandations :**
* **Durcissement SSH :** Désactiver l'authentification par mot de passe au profit de clés SSH, désactiver l'accès root à distance, et utiliser `HashKnownHosts` dans la configuration SSH.
* **Gestion des accès :** Implémenter l'authentification multifacteur (MFA) et utiliser des solutions comme HashiCorp Vault pour générer des certificats SSH éphémères signés, limitant ainsi la durée de vie des accès.
* **Contrôles réseau :** Appliquer une politique "deny by default" (tout refuser par défaut), mettre en place un filtrage d'entrée/sortie, et utiliser des pare-feu couplés à des systèmes de détection/prévention d'intrusion (IDS/IPS).
* **Surveillance :** Utiliser un SIEM pour centraliser et corréler les logs (syslog). Déployer des outils comme `Fail2Ban` pour bloquer automatiquement les adresses IP suspectes après des échecs de connexion répétés.
* **Analyse :** Utiliser des outils d'analyse dynamique comme `FakeNet-NG` pour observer le comportement réseau des binaires suspects en environnement contrôlé.

---
[Source](https://isc.sans.edu/diary/rss/33426){:target="_blank"}
