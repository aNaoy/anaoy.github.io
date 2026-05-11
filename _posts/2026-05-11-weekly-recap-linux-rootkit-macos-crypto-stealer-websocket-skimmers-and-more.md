---
title: '⚡ Weekly Recap: Linux Rootkit, macOS Crypto Stealer, WebSocket Skimmers and More'
date: 2026-05-11
permalink: /posts/2026/05/11/weekly-recap-linux-rootkit-macos-crypto-stealer-websocket-skimmers-and-more/
tags:
- veille-cyber
- hackernews
---
### État des lieux de la cybersécurité : Menaces persistantes et vecteurs d'attaques

Cette semaine a été marquée par une recrudescence d'attaques ciblant les chaînes d'approvisionnement, des vulnérabilités critiques exploitées activement et une utilisation sophistiquée de l'ingénierie sociale (notamment le *ClickFix*).

#### **Points clés**
*   **Chaînes d'approvisionnement :** Les sites officiels (JDownloader, DAEMON Tools) sont détournés pour distribuer des logiciels malveillants.
*   **Infrastructure cloud :** Des campagnes (PCPJack) ciblent systématiquement les environnements cloud en éliminant les malwares concurrents pour voler des secrets industriels.
*   **Ingénierie sociale :** La technique du *ClickFix* domine, manipulant les utilisateurs via de fausses vérifications Cloudflare ou de fausses invitations à des entretiens pour installer des infostealers sur Windows et macOS.
*   **Espionnage :** Des groupes étatiques (MuddyWater) masquent leurs activités d'espionnage sous couvert de campagnes de ransomware (Chaos).
*   **IA et automatisation :** L'émergence d'outils comme *ConsentFix v3* automatise le détournement de comptes Microsoft, tandis que les attaquants exploitent des vulnérabilités dans les agents IA (Cline).

#### **Vulnérabilités critiques à surveiller**
*   **Ivanti EPMM :** [CVE-2026-6973](https://thehackernews.com/2026/05/ivanti-epmm-cve-2026-6973-rce-under.html) (RCE par validation d'entrée défaillante).
*   **Palo Alto Networks PAN-OS :** [CVE-2026-0300](https://thehackernews.com/2026/05/pan-os-rce-exploit-under-active-use.html) (Corruption mémoire permettant une exécution de code root).
*   **Cline (Kanban Server) :** Vulnérabilité critique (Score 9.7/10) due à l'absence de validation d'origine sur les WebSockets.
*   **Autres CVE notables :** [CVE-2026-29014](https://thehackernews.com/2026/05/metinfo-cms-cve-2026-29014-exploited.html) (MetInfo), [CVE-2026-22679](https://thehackernews.com/2026/05/weaver-e-cology-rce-flaw-cve-2026-22679.html) (Weaver E-cology) et [CVE-2026-4670 / 5174](https://thehackernews.com/2026/05/progress-patches-critical-moveit.html) (Progress MOVEit).

#### **Recommandations**
1.  **Application des correctifs :** Prioriser le patch des failles mentionnées (Ivanti et Palo Alto en tête).
2.  **Méfiance accrue :** Ne pas exécuter de commandes dans le terminal sur demande d'un site web (technique *ClickFix*).
3.  **Surveillance des logs :** Scruter les accès inhabituels vers les outils RMM (Remote Monitoring and Management) comme *SimpleHelp* ou *ScreenConnect*.
4.  **Gestion des accès :** Renforcer la sécurité des comptes OIDC/OAuth pour contrer les campagnes de type *ConsentFix*.
5.  **Audit des outils IA :** S'assurer que les agents de développement IA locaux (ex: Cline) sont mis à jour vers des versions sécurisées et ne sont pas accessibles via des navigateurs non autorisés.

---
[Source](https://thehackernews.com/2026/05/weekly-recap-linux-rootkit-macos-crypto.html){:target="_blank"}
