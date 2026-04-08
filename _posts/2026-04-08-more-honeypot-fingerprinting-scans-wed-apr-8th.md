---
title: 'More Honeypot Fingerprinting Scans, (Wed, Apr 8th)'
date: 2026-04-08
permalink: /posts/2026/04/08/more-honeypot-fingerprinting-scans-wed-apr-8th/
tags:
- veille-cyber
- sans-isc
---
### Détection et identification des honeypots par les attaquants

Les attaquants utilisent diverses techniques pour identifier les honeypots « à interaction moyenne » (comme Cowrie) en exploitant les limites de leur simulation.

**Points clés :**
* **Simulation incomplète :** Les honeypots simulent des systèmes réels qui ne répondent pas toujours de manière authentique aux commandes complexes ou aux installations de paquets.
* **Empreintes SSH :** L'analyse des artefacts SSH, tels que les suites de chiffrement supportées, permet de trahir la nature artificielle du système.
* **Authentification piégée :** Certains attaquants testent des combinaisons identifiant/mot de passe absurdes ou explicites (ex: « honeypot » / « indexer »). Si ces accès sont acceptés, l'attaquant confirme immédiatement qu'il s'agit d'un système de leurre.
* **Stratégie de recherche :** L'objectif des attaquants est d'exclure les honeypots de leurs listes de cibles pour se concentrer sur des systèmes réels.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car il s'agit d'une faiblesse inhérente à la conception des logiciels de simulation (honeypots à interaction moyenne).

**Recommandations :**
* **Acceptation des limites :** Il n'est pas toujours nécessaire de masquer totalement un honeypot. Les recherches axées sur les scans à grande échelle restent pertinentes malgré la détection par les attaquants.
* **Infrastructure dynamique :** Utiliser des réseaux domestiques avec des IP dynamiques permet de rendre obsolètes les listes noires générées par les attaquants, limitant ainsi l'impact de leur identification.

---
[Source](https://isc.sans.edu/diary/rss/32878){:target="_blank"}
