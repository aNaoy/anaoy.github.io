---
title: 'The Gentlemen RaaS Uses GentleKiller EDR Framework Targeting 400 Security Processes'
date: 2026-06-19
permalink: /posts/2026/06/19/the-gentlemen-raas-uses-gentlekiller-edr-framework-targeting-400-security-processes/
tags:
- veille-cyber
- hackernews
---
### Menace émergente : Le framework « GentleKiller » du groupe The Gentlemen

Le groupe de ransomware-as-a-service (RaaS) « The Gentlemen » a mis en place un écosystème hautement sophistiqué pour neutraliser les solutions de sécurité (EDR) avant toute attaque. Centralisée autour du framework **GentleKiller**, cette opération fournit à ses affiliés des outils standardisés capables de cibler plus de 400 processus de sécurité.

**Points clés :**
*   **Agilité tactique :** Le groupe intègre des preuves de concept (PoC) d'exploits en quelques jours seulement après leur publication publique.
*   **Technique BYOVD (Bring Your Own Vulnerable Driver) :** Les attaquants exploitent des pilotes légitimes vulnérables pour obtenir des privilèges système et désactiver les défenses.
*   **Imposture :** Les outils utilisent des certificats numériques, icônes et noms de fichiers usurpés pour imiter des éditeurs de logiciels de sécurité légitimes.
*   **Diversification :** En plus des ransomwares, le groupe déploie « OxideHarvest », un voleur d'identifiants basé sur Rust capable d'exfiltrer les données de la majorité des navigateurs web.

**Pilotes vulnérables exploités :**
Le groupe abuse notamment de pilotes tels que `PoisonX.sys` (utilisé pour contrer CrowdStrike), `eb.sys` (Kaspersky), `GameDriverX64.sys` (Valorant), ainsi que divers pilotes liés à des logiciels de nettoyage ou de réseau.

**Vulnérabilités associées :**
*   Le rapport souligne une vulnérabilité critique de **contournement de Secure Boot** via des applications UEFI signées par des constructeurs (Acer, AMD, ASUS, GIGABYTE, etc.). 
*   *Note : Les correctifs passent par la mise à jour de la base de données de signatures interdites (DBX) de l'UEFI.*

**Recommandations :**
*   **Mise à jour du firmware :** Appliquer les correctifs UEFI fournis par les constructeurs et mettre à jour la base de données DBX pour révoquer les certificats vulnérables.
*   **Surveillance des pilotes :** Auditer les pilotes chargés sur les points de terminaison et restreindre l'utilisation de pilotes tiers non essentiels via des politiques de contrôle d'application (AppLocker ou Windows Defender Application Control).
*   **Protection des accès :** Étant donné que ces attaques nécessitent souvent des privilèges administratifs, le principe du moindre privilège est crucial pour limiter l'impact d'une exécution de pilote malveillant.
*   **Détection comportementale :** Surveiller les processus tentant de terminer les services EDR, particulièrement ceux utilisant des noms de fichiers usurpés ou signés de manière suspecte.

---
[Source](https://thehackernews.com/2026/06/the-gentlemen-raas-uses-gentlekiller.html){:target="_blank"}
