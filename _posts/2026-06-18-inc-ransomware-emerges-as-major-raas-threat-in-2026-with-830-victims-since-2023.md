---
title: 'INC Ransomware Emerges as Major RaaS Threat in 2026 with 830+ Victims Since 2023'
date: 2026-06-18
permalink: /posts/2026/06/18/inc-ransomware-emerges-as-major-raas-threat-in-2026-with-830-victims-since-2023/
tags:
- veille-cyber
- hackernews
---
### Montée en puissance du ransomware INC : une menace RaaS majeure

Le groupe INC Ransom est devenu l'un des acteurs les plus prolifiques du cybercrime, avec plus de 830 victimes recensées depuis août 2023. Profitant de la disparition d'anciens groupes comme LockBit et BlackCat, INC a structuré son opération sous forme de Ransomware-as-a-Service (RaaS) et multiplie les attaques, principalement aux États-Unis, contre les secteurs de la santé, du droit et de l'industrie.

**Points clés**
*   **Évolution technique :** Le groupe a réécrit ses chiffreurs en Rust pour faciliter le développement multiplateforme (Windows/Linux/ESXi) et compliquer l'analyse.
*   **Mode opératoire :** Utilisation intensive de la technique "Living-off-the-Land" (LOLBins), d'outils d'administration à distance (RMM) légitimes et de tactiques BYOVD (*Bring Your Own Vulnerable Driver*) pour neutraliser les antivirus.
*   **Ciblage spécifique :** Priorité aux serveurs de sauvegarde Veeam, avec des outils capables de déchiffrer les identifiants protégés par DPAPI.
*   **Double extorsion :** Exfiltration massive de données via Rclone avant le déploiement du chiffreur.

**Vulnérabilités exploitées pour l'accès initial**
*   **CVE-2023-3519** & **CVE-2025-5777** : Citrix NetScaler.
*   **CVE-2023-48788** : Fortinet EMS.
*   **CVE-2024-57727** : SimpleHelp.

**Recommandations**
*   **Correction et durcissement :** Appliquer immédiatement les correctifs sur les équipements de périphérie (Edge devices) et les applications exposées.
*   **Sécurisation des sauvegardes :** Isoler les serveurs de sauvegarde (Veeam) et renforcer la protection des identifiants stockés localement.
*   **Surveillance réseau :** Détecter l'usage anormal d'outils RMM (AnyDesk, TeamViewer, ScreenConnect) et d'outils d'administration système utilisés à des fins malveillantes.
*   **Gestion des accès :** Appliquer le principe du moindre privilège pour limiter les mouvements latéraux facilités par l'usage détourné de PsExec ou du protocole RDP.

---
[Source](https://thehackernews.com/2026/06/inc-ransomware-claims-830-victims-since.html){:target="_blank"}
