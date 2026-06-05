---
title: 'New Threat Cluster OP-512 Targets Microsoft IIS Servers with Custom Web Shell Framework'
date: 2026-06-05
permalink: /posts/2026/06/05/new-threat-cluster-op-512-targets-microsoft-iis-servers-with-custom-web-shell-framework/
tags:
- veille-cyber
- hackernews
---
### OP-512 : Une nouvelle menace ciblant les serveurs Microsoft IIS

Le groupe de cyberespionnage **OP-512**, potentiellement lié à la Chine, déploie un framework de web shells sophistiqué pour compromettre des serveurs Microsoft Internet Information Services (IIS). Ce cluster se distingue par l'utilisation d'outils sur mesure conçus pour contourner les méthodes de détection classiques.

**Points clés :**
*   **Technique d'évasion :** Utilisation du « timestomping » pour manipuler les métadonnées des fichiers (date de création/modification) afin de se fondre dans l'historique du système.
*   **Framework sur mesure :** Les web shells sont générés de manière unique pour chaque cible, incluent des contrôles cryptographiques et un mécanisme d'auto-signalement pour une gestion centralisée.
*   **Mode opératoire :** L'attaque repose sur une exécution rapide (« sprint ») via le processus `w3wp.exe`, permettant une prise de contrôle totale (gestion de fichiers et exécution de commandes) avant toute réaction défensive.
*   **Escalade de privilèges :** Tentatives d'élévation de droits au niveau SYSTEM via l'exploitation de vulnérabilités de type « Potato Suite ».

**Vulnérabilités :**
L'attaque cible principalement des serveurs IIS obsolètes, notamment ceux utilisant **Windows Server 2016** avec des versions de **.NET Framework (4.0)** arrivées en fin de vie. Bien qu'aucune CVE spécifique ne soit citée pour l'entrée initiale, le risque est exacerbé par l'utilisation de logiciels non supportés.

**Recommandations :**
*   **Mise à jour système :** Migrer les serveurs IIS tournant sur des versions obsolètes de Windows Server et du .NET Framework vers des versions supportées et sécurisées.
*   **Surveillance accrue :** Surveiller les comportements anormaux du processus `w3wp.exe`, notamment les écritures de fichiers inhabituelles dans les répertoires d'upload.
*   **Analyse DNS :** Surveiller les requêtes DNS sortantes vers des domaines inconnus ou suspects, souvent utilisées par les web shells pour signaler leur présence.
*   **Durcissement :** Appliquer le principe du moindre privilège pour limiter l'impact en cas d'élévation de droits (protection contre la « Potato Suite »).
*   **Détection proactive :** Ne pas se reposer uniquement sur des signatures connues, car OP-512 utilise des outils personnalisés qui ne correspondent pas aux empreintes des menaces habituelles.

---
[Source](https://thehackernews.com/2026/06/new-threat-cluster-op-512-targets.html){:target="_blank"}
