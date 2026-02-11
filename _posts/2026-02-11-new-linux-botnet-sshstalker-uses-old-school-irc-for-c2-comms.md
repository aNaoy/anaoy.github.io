---
title: 'New Linux botnet SSHStalker uses old-school IRC for C2 comms'
date: 2026-02-11
permalink: /posts/2026/02/11/new-linux-botnet-sshstalker-uses-old-school-irc-for-c2-comms/
tags:
- veille-cyber
- bleepingcomp
---
### SSHStalker : Une botnet Linux s'appuyant sur des méthodes éprouvées

Une nouvelle menace, baptisée SSHStalker, cible les systèmes Linux en exploitant le protocole IRC (Internet Relay Chat) pour ses communications de commande et contrôle (C2). Contrairement aux approches modernes, SSHStalker privilégie la résilience, l'évolutivité et le faible coût en utilisant des techniques plus anciennes, telles que des bots écrits en C et une redondance multi-serveurs/canaux IRC.

Cette botnet utilise des scans SSH bruyants et des tâches cron d'une minute pour s'établir et se propager. Elle a également été observée exploitant de vieilles vulnérabilités du noyau Linux, datant de 2009-2010, pour élever ses privilèges. Son objectif final inclut la récolte de clés AWS, le minage de cryptomonnaies (notamment avec PhoenixMiner) et potentiellement des attaques par déni de service distribué (DDoS), bien que ces dernières n'aient pas encore été observées.

La propagation initiale se fait par des scans et des attaques par force brute SSH automatisés, se camouflant parfois en outils légitimes comme nmap. Une fois un système compromis, il télécharge un compilateur (GCC) pour construire ses charges utiles sur la machine victime, rendant ainsi les actions plus difficiles à tracer. Les systèmes infectés servent ensuite à trouver de nouvelles cibles SSH, créant un effet d'essaim. Les chercheurs ont identifié près de 7 000 scans de bots dans les données analysées, principalement dirigés vers l'infrastructure cloud d'Oracle.

Bien qu'aucune attribution spécifique n'ait été faite, des similitudes ont été notées avec l'écosystème de botnets Outlaw/Maxlas.

**Points Clés :**

*   **Protocole C2 désuet :** Utilisation d'IRC pour la communication de commande et contrôle, privilégiant la simplicité et la résilience.
*   **Méthodes d'infection variées :** Scans SSH bruyants, force brute, et exploitation de vieilles vulnérabilités du noyau Linux pour l'escalade de privilèges.
*   **Compilation sur l'hôte :** Utilisation de GCC sur les machines compromises pour compiler les charges utiles, améliorant la portabilité et l'évasion.
*   **Persistance par Cron :** Tâches cron fréquentes (toutes les 60 secondes) pour assurer le maintien des processus du bot.
*   **Objectifs multiples :** Vol de clés AWS, minage de cryptomonnaies, et potentiel pour des attaques DDoS.
*   **Propagation à la manière d'un ver :** Les machines compromises scannent activement de nouvelles cibles SSH.

**Vulnérabilités exploitées :**

*   Exploits pour 16 CVEs ciblant des versions du noyau Linux datant de 2009-2010. Les CVEs spécifiques ne sont pas listés dans l'article, mais elles sont utilisées pour l'escalade de privilèges après un accès initial par brute force SSH.

**Recommandations :**

*   Désactiver l'authentification par mot de passe SSH.
*   Supprimer les compilateurs (comme GCC) des images de production.
*   Mettre en place un filtrage sortant (egress filtering).
*   Restreindre l'exécution depuis des répertoires sensibles comme `/dev/shm`.
*   Surveiller l'installation et l'exécution de compilateurs sur les serveurs de production.
*   Mettre en place des alertes pour les connexions sortantes de type IRC.
*   Identifier les tâches cron avec des cycles d'exécution courts depuis des chemins inhabituels comme des indicateurs potentiels.

---
[Source](https://www.bleepingcomputer.com/news/security/new-linux-botnet-sshstalker-uses-old-school-irc-for-c2-comms/){:target="_blank"}
