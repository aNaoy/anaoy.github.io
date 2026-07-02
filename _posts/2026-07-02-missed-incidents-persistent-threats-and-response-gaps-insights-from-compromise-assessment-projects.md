---
title: 'Missed incidents, persistent threats, and response gaps: Insights from compromise assessment projects'
date: 2026-07-02
permalink: /posts/2026/07/02/missed-incidents-persistent-threats-and-response-gaps-insights-from-compromise-assessment-projects/
tags:
- veille-cyber
- securelist
---
### Enseignements des évaluations de compromission 2025

Les évaluations de compromission réalisées en 2025 révèlent une lacune majeure dans la détection des menaces : 30,8 % des incidents, dont 52 % des cas à haute criticité, sont restés actifs plus de trois mois avant d'être découverts. Le record de persistance identifié atteint quatre ans.

#### Points clés
*   **Défaut de détection :** 60 % des incidents ont été manqués par les outils en place faute d'alertes pertinentes. 
*   **Réactivité limitée :** Les enquêtes post-incident classiques échouent souvent à identifier des points de persistance latents, contrairement aux audits proactifs.
*   **Persistance via les sauvegardes :** 40 % des shells web découverts résidaient dans des sauvegardes, réinfectant les systèmes après chaque nettoyage.
*   **Abus d'outils légitimes :** L'usage détourné de binaires natifs (LoLBins) et d'outils d'administration à distance est systématique dans les incidents détectés.
*   **Manque de maturité opérationnelle :** L'absence de surveillance 24/7 et de *threat hunting* (chasse aux menaces) augmente la probabilité d'incidents critiques à 84-86 %.

#### Vulnérabilités notables
*   **MS17-010 (EternalBlue) :** Toujours exploitée par des campagnes de crypto-minage (ex: *NSABuffMiner*) quatre ans après la publication du correctif.
*   **Défauts de configuration GPO :** Partages réseau avec des droits "Everyone – Full Control" permettant une élévation de privilèges et une propagation latérale automatique.
*   **Outils d'IA générative :** Fuites de données confidentielles via des extensions (ex: Claude Code) capturant automatiquement des clichés du système de fichiers.

#### Recommandations stratégiques
1.  **Validation des outils :** Effectuer un audit de santé des sondes de détection (EPP/EDR) et de la pertinence des règles sous 30 jours.
2.  **Triage manuel :** Mettre en place une équipe dédiée à la validation des alertes de faible confiance, souvent ignorées par les systèmes automatisés.
3.  **Surveillance continue :** Passer d'un modèle "installé et oublié" à une surveillance active avec *threat hunting* basé sur l'analyse comportementale plutôt que sur de simples listes de blocage.
4.  **Hygiène des processus :** 
    *   Durcir les permissions des partages réseau et auditer les GPO.
    *   Renforcer la gestion des vulnérabilités et l'inventaire des actifs (incluant les machines cloud isolées).
    *   Intégrer des exercices de simulation (*tabletop exercises*) pour tester la communication entre les équipes techniques lors d'une crise.
5.  **Maturité interne :** Développer des compétences internes en forensique et ingénierie inverse, car la dépendance exclusive à des prestataires externes sans gouvernance interne est corrélée à une plus grande criticité des incidents.

---
[Source](https://securelist.com/compromise-assessment-findings-2025/120542/){:target="_blank"}
