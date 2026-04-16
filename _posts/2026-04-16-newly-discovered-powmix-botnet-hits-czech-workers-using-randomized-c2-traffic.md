---
title: 'Newly Discovered PowMix Botnet Hits Czech Workers Using Randomized C2 Traffic'
date: 2026-04-16
permalink: /posts/2026/04/16/newly-discovered-powmix-botnet-hits-czech-workers-using-randomized-c2-traffic/
tags:
- veille-cyber
- hackernews
---
### Analyse du botnet PowMix : Menaces et évasion

Le botnet **PowMix**, actif depuis décembre 2025, cible les travailleurs en République tchèque via des campagnes de phishing sophistiquées. Ce malware se distingue par des techniques avancées d'évasion et une gestion dynamique de son infrastructure de commande et contrôle (C2).

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de fichiers ZIP malveillants contenant des raccourcis Windows (.LNK) qui exécutent des loaders PowerShell. Le malware s'exécute directement en mémoire.
*   **Techniques d'évasion :** Utilisation de la commande `Get-Random` pour générer des intervalles de communication (jitter) irréguliers et masquer les signatures réseau. Le trafic C2 imite des appels d'API REST légitimes.
*   **Persistance et leurres :** Utilisation de tâches planifiées pour la persistance et ouverture simultanée de faux documents de conformité pour distraire l'utilisateur.
*   **Modularité :** Possibilité de mettre à jour dynamiquement les domaines C2 et d'exécuter des charges utiles arbitraires.

**Vulnérabilités :**
*   Bien que l'article mentionne que le botnet RondoDox exploite plus de 170 vulnérabilités connues (sans liste exhaustive), PowMix se concentre sur l'exploitation du facteur humain via le phishing et l'utilisation de PowerShell. Aucune CVE spécifique n'est associée à l'exécution initiale de PowMix, qui repose sur l'exécution de code par l'utilisateur.

**Recommandations :**
*   **Sensibilisation :** Former les employés à la méfiance envers les pièces jointes non sollicitées, particulièrement les fichiers compressés (.ZIP) contenant des raccourcis.
*   **Filtrage PowerShell :** Restreindre ou surveiller étroitement l'exécution des scripts PowerShell au sein de l'environnement de travail.
*   **Segmentation et surveillance réseau :** Mettre en place une surveillance du trafic sortant pour détecter des beacons (signaux) irréguliers et des requêtes vers des domaines suspects ou non répertoriés.
*   **Analyse de processus :** Déployer des solutions EDR (Endpoint Detection and Response) capables d'identifier les comportements suspects, comme le déploiement de tâches planifiées par des processus inhabituels ou des tentatives de suppression de traces.

---
[Source](https://thehackernews.com/2026/04/newly-discovered-powmix-botnet-hits.html){:target="_blank"}
