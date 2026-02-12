---
title: 'Crazy ransomware gang abuses employee monitoring tool in attacks'
date: 2026-02-12
permalink: /posts/2026/02/12/crazy-ransomware-gang-abuses-employee-monitoring-tool-in-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Une Gang de Ransomware Exploite des Outils de Surveillance pour des Attaques Sophistiquées**

Des acteurs malveillants associés au groupe Crazy ransomware tirent parti de logiciels légitimes de surveillance d'employés et d'outils d'assistance à distance comme SimpleHelp pour établir une persistance dans les réseaux d'entreprise, échapper à la détection et préparer des déploiements de ransomware.

Des chercheurs ont observé que ces attaquants installaient "Net Monitor for Employees Professional" via l'utilitaire Windows Installer (`msiexec.exe`), leur permettant d'obtenir un accès interactif complet aux systèmes compromis. Ils cherchaient également à réactiver le compte administrateur local avec la commande `net user administrator /active:yes`. Pour assurer une persistance redondante, SimpleHelp était installé via PowerShell, parfois déguisé sous des noms de fichiers similaires à des exécutables légitimes de Visual Studio ou de OneDrive. Les attaquants utilisaient ces outils pour exécuter des commandes, transférer des fichiers et surveiller l'activité système en temps réel, désactivant même Windows Defender.

Dans certains cas, la configuration de SimpleHelp incluait la surveillance de mots-clés liés aux portefeuilles de cryptomonnaies et aux outils d'accès à distance, afin de détecter les activités sensibles avant le déploiement du ransomware et le vol potentiel de cryptomonnaies. L'utilisation combinée de plusieurs outils d'accès à distance assure aux attaquants une redondance de leur présence, même si un outil est découvert.

Bien qu'une seule intrusion ait conduit au déploiement de Crazy ransomware, les indices tels que la réutilisation de noms de fichiers et d'infrastructures de commande et de contrôle suggèrent l'implication du même acteur. L'exploitation d'outils de gestion et de surveillance légitimes est une tactique croissante pour se fondre dans le trafic réseau légitime.

**Points clés:**

*   Utilisation de logiciels de surveillance d'employés ("Net Monitor for Employees Professional") et d'outils d'assistance à distance (SimpleHelp) par des groupes de ransomware.
*   Objectif de persistance, d'évasion de détection et de préparation au déploiement de ransomware.
*   Désactivation de la sécurité (Windows Defender) et activation de comptes administratifs.
*   Surveillance active de mots-clés sensibles (cryptomonnaies, accès à distance) pour identifier les cibles potentielles.
*   L'exploitation d'outils légitimes aide les attaquants à se dissimuler.

**Vulnérabilités et Tactiques:**

*   Installation et abus de "Net Monitor for Employees Professional" pour un contrôle total des systèmes.
*   Utilisation de SimpleHelp pour une persistance redondante et un accès à distance caché.
*   Tentatives de réactivation du compte administrateur local.
*   Désactivation des protections antivirus (Windows Defender).
*   Techniques d'obfuscation des noms de fichiers pour les exécutables malveillants.
*   Utilisation de politiques de surveillance ciblées pour détecter les activités de cryptomonnaie et d'accès à distance.
*   Les compromissions initiales ont été facilitées par des identifiants SSL VPN compromis.

**Recommandations:**

*   Surveiller attentivement les installations non autorisées d'outils de surveillance et de support à distance.
*   Mettre en œuvre l'authentification multifacteur (MFA) sur tous les services d'accès à distance (y compris les VPN SSL) pour prévenir les compromissions d'identifiants.
*   Veiller à la bonne configuration et à la protection des outils d'administration légitimes.

---
[Source](https://www.bleepingcomputer.com/news/security/crazy-ransomware-gang-abuses-employee-monitoring-tool-in-attacks/){:target="_blank"}
