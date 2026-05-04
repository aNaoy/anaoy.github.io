---
title: 'Hacking Polymarket'
date: 2026-05-04
permalink: /posts/2026/05/04/hacking-polymarket/
tags:
- veille-cyber
- schneier
---
### Vulnérabilités et manipulation du système de prédiction Polymarket

La plateforme de paris en ligne Polymarket fait face à des failles structurelles majeures liées à sa dépendance envers des données du monde réel (« oracles ») et à l'absence de régulation efficace :

**Points clés**
*   **Manipulation physique :** Les participants altèrent directement les capteurs de données (ex: usage de sèche-cheveux sur des stations météo) pour truquer les résultats des paris.
*   **Intimidation :** Les parieurs harcèlent les sources d'information (journalistes, témoins) pour influencer la résolution des marchés en leur faveur.
*   **Délits d'initiés :** La plateforme est fortement exposée à l'utilisation d'informations privilégiées pour fausser les cotes, compromettant l'intégrité des échanges.
*   **Absence de CVE :** Les risques identifiés ne découlent pas de vulnérabilités logicielles classiques (exploitables par des CVE), mais de vulnérabilités conceptuelles inhérentes à la manière dont la plateforme vérifie les événements réels.

**Recommandations**
*   **Fiabilisation des sources :** Mettre en place des mécanismes de validation multi-sources et redondants pour les données d'entrée afin d'éviter la dépendance à un seul capteur ou témoin.
*   **Sécurisation physique :** Renforcer la protection et l'intégrité matérielle des capteurs utilisés comme sources de vérité.
*   **Surveillance et conformité :** Implémenter des outils d'analyse comportementale pour détecter et sanctionner les activités suspectes ou les délits d'initiés.
*   **Cadre éthique et légal :** Développer une gouvernance stricte pour protéger les tiers (journalistes, sources) contre les menaces liées aux enjeux financiers de la plateforme.

---
[Source](https://www.schneier.com/blog/archives/2026/05/hacking-polymarket.html){:target="_blank"}
