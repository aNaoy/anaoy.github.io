---
title: 'Google Disrupts UNC2814 GRIDTIDE Campaign After 53 Breaches Across 42 Countries'
date: 2026-02-25
permalink: /posts/2026/02/25/google-disrupts-unc2814-gridtide-campaign-after-53-breaches-across-42-countries/
tags:
- veille-cyber
- hackernews
---
**Démantèlement de la Campagne GRIDTIDE, Opération d'Espionnage à Grande Échelle**

Une opération d'espionnage cybernétique d'envergure, attribuée au groupe UNC2814 et baptisée GRIDTIDE, a été perturbée grâce à une collaboration impliquant Google et d'autres acteurs du secteur. Cette campagne aurait compromis au moins 53 organisations dans 42 pays, ciblant principalement des gouvernements internationaux et des entreprises de télécommunications en Afrique, en Asie et dans les Amériques. Le groupe, suivi depuis 2017, est suspecté d'opérer depuis la Chine.

L'infrastructure de commande et de contrôle (C2) reposait sur l'utilisation détournée des API de services cloud, notamment Google Sheets, pour masquer le trafic malveillant sous des requêtes légitimes. Le malware principal, GRIDTIDE, utilise ces API pour échanger des commandes et des données, y compris des fichiers. L'accès initial de UNC2814 reste sous investigation, mais il est établi que le groupe exploite des serveurs web et des systèmes périphériques.

**Points Clés:**

*   **Acteur:** UNC2814 (probablement lié à la Chine)
*   **Campagne:** GRIDTIDE
*   **Cibles:** Gouvernements, télécommunications (Afrique, Asie, Amériques)
*   **Portée:** 53 organisations compromises dans 42 pays, avec des suspicions dans plus de 20 autres.
*   **Technique de C2:** Utilisation des API de services cloud (notamment Google Sheets) pour masquer le trafic.
*   **Malware Principal:** GRIDTIDE, un malware C-basé utilisant les API pour le transfert de données et l'exécution de commandes.
*   **Méthodes d'Action:** Exploitation de serveurs web, systèmes périphériques, utilisation de comptes de service pour le mouvement latéral via SSH, exploitation de binaires "living-off-the-land" (LotL) pour la reconnaissance et l'escalade de privilèges, et établissement de persistance via la création de services système. Utilisation de SoftEther VPN Bridge pour des connexions sortantes chiffrées.
*   **Objectif:** Espionnage, potentiellement axé sur la collecte d'informations personnelles identifiables (PII).
*   **Action de Google:** Démantèlement de l'infrastructure de UNC2814, désactivation des accès aux API Google Sheets compromis et notification des victimes.

**Vulnérabilités et Exploits:**

*   Les détails spécifiques des vulnérabilités exploitées pour l'accès initial ne sont pas précisés, mais l'article mentionne une exploitation des serveurs web et des systèmes périphériques.

**Recommandations:**

*   **Surveillance accrue des systèmes périphériques et des serveurs web:** Ces points d'entrée sont régulièrement ciblés par des acteurs malveillants.
*   **Renforcement des mécanismes de sécurité pour les services cloud:** Une attention particulière doit être portée à l'utilisation et à la sécurisation des API, en surveillant les trafics inhabituels.
*   **Mise en place d'une détection de logiciels malveillants sur les points d'accès réseau (edge devices):** Ces appareils manquent souvent de protection, ce qui en fait des cibles attrayantes.
*   **Surveillance des activités suspectes utilisant des VPN légitimes à des fins malveillantes:** L'utilisation de SoftEther VPN dans ce contexte souligne la nécessité de cette vigilance.
*   **Mise en place de systèmes de détection d'intrusion et de surveillance comportementale:** Ces systèmes peuvent aider à identifier l'utilisation de binaires LotL et d'autres techniques d'évasion.

---
[Source](https://thehackernews.com/2026/02/google-disrupts-unc2814-gridtide.html){:target="_blank"}
