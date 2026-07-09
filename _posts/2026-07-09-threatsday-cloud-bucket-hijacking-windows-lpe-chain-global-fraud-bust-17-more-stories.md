---
title: 'ThreatsDay: Cloud Bucket Hijacking, Windows LPE Chain, Global Fraud Bust + 17 More Stories'
date: 2026-07-09
permalink: /posts/2026/07/09/threatsday-cloud-bucket-hijacking-windows-lpe-chain-global-fraud-bust-17-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : De la compromission cloud à l'ingénierie sociale

Cette semaine est marquée par une recrudescence d'attaques utilisant des vecteurs "silencieux" exploitant les configurations par défaut et la confiance accordée aux outils légitimes.

#### Points clés et vulnérabilités
*   **Infrastructure Cloud & Hijacking :** Une faille architecturale permet de détourner des flux de données en recréant des "buckets" de stockage portant le même nom qu'un service légitime. De plus, des risques d'élévation de privilèges ("Agent God Mode") ont été identifiés dans les outils d'automatisation AWS (AgentCore).
*   **Vulnérabilités critiques :**
    *   **CVE-2026-9181 (CVSS 9.8) :** Accès non authentifié à des fichiers sensibles sur **Esri ArcGIS Server** via une traversée de répertoire.
    *   **CVE-2025-59200 :** Exploitation du service **DsSvc** sous Windows pour usurper un serveur RPC et élever ses privilèges.
    *   **Série CVE-2022/2024 (Réaltek) :** Vulnérabilités dans les pilotes **RtsPer.sys** permettant une lecture/écriture arbitraire en mémoire noyau (DMA).
*   **Logiciels malveillants et supply chain :**
    *   **Typosquattage :** 17 paquets malveillants sur npm/PyPI imitent des SDK de paiement (Paysafe, Skrill) pour exfiltrer des secrets de développeurs.
    *   **Injection furtive :** La technique *Process Parameter Poisoning* (P³) permet d'injecter du code sans suspendre les processus, contournant ainsi les détections classiques.
*   **Menaces liées à l'IA :** Les versions 2.1.91 à 2.1.196 de **Claude Code** ont été signalées pour une collecte non autorisée de données identifiables. Les systèmes multi-agents sont également vulnérables aux injections de prompt menant à une exfiltration de données.
*   **Campagnes actives :** Recrudescence de l'ingénierie sociale via de faux supports informatiques (Microsoft Teams) pour installer des RAT (EtherRAT, Remcos) et de campagnes de phishing ciblant Meta Business Manager.

#### Recommandations
1.  **Sécurisation du Cloud :** Implémenter des contrôles de sortie (egress) stricts pour empêcher l'exfiltration de données par des agents IA ou des processus compromis.
2.  **Gestion des accès :** Auditer les configurations ADFS pour éviter la dérive de configuration (ghost keys) permettant la falsification de jetons SAML.
3.  **Surveillance des "chemins normaux" :** Ne pas se contenter de détecter des comportements anormaux. Surveiller étroitement les noms de paquets (typosquattage), les autorisations excessives accordées aux outils (Principes du moindre privilège) et les flux de trafic sortants.
4.  **Mises à jour :** Appliquer les correctifs pour ArcGIS Server, mettre à jour les pilotes Realtek et installer les versions sécurisées des outils de développement.
5.  **Hygiène numérique :** Sensibiliser les utilisateurs à la méfiance envers les appels de support technique spontanés et les notifications de remboursement fiscal, vecteurs privilégiés pour le déploiement de RAT.

---
[Source](https://thehackernews.com/2026/07/threatsday-cloud-bucket-hijacking.html){:target="_blank"}
