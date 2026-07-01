---
title: 'Turning Indicators into Intelligence in OpenCTI with Criminal IP'
date: 2026-07-01
permalink: /posts/2026/07/01/turning-indicators-into-intelligence-in-opencti-with-criminal-ip/
tags:
- veille-cyber
- bleepingcomp
---
### Optimisation du Renseignement Cyber : Intégration de Criminal IP dans OpenCTI

L'intégration de Criminal IP au sein de la plateforme OpenCTI permet de transformer des indicateurs de compromission (IP, domaines, URL) isolés en une intelligence structurée et contextuelle. En automatisant l'enrichissement des données, cette solution aide les équipes de sécurité à mieux prioriser les menaces et à cartographier les infrastructures attaquantes.

**Points clés :**
*   **Enrichissement automatisé :** Ajout automatique de données de réputation, de signaux comportementaux et d'analyses de phishing directement dans le graphe de connaissances d'OpenCTI.
*   **Scoring bidimensionnel :** Évaluation des risques basée sur une double perspective (entrante et sortante), offrant une vision plus fine que les modèles de réputation classiques.
*   **Visibilité sur les surfaces d'attaque :** Corrélation entre les services exposés et les vulnérabilités connues pour identifier rapidement les actifs exploitables.
*   **Analyse d'infrastructure :** Capacité à effectuer des pivots entre les indicateurs grâce à des relations structurées (systèmes autonomes, géolocalisation, domaines associés).
*   **Analyse avancée du Phishing :** Détection précise des techniques de récolte d'identifiants et d'usurpation d'identité avec des scores de confiance dédiés.

**Vulnérabilités :**
*   L'intégration corrèle automatiquement les adresses IP avec les **CVE (Common Vulnerabilities and Exposures)** associées aux services exposés. Cela permet aux analystes de savoir si une infrastructure malveillante est vulnérable à des exploits spécifiques, bien que l'article ne liste pas de CVE individuelles, se concentrant sur la méthodologie de corrélation automatique.

**Recommandations :**
*   **Priorisation des alertes :** Utiliser les scores de risque contextuels pour filtrer les faux positifs dans le SOC et concentrer les ressources sur les infrastructures à haute probabilité de malveillance.
*   **Chasse aux menaces (Threat Hunting) :** Exploiter les relations enrichies (liens entre serveurs, domaines et AS) pour identifier des clusters d'infrastructures liés à des campagnes d'attaques spécifiques.
*   **Validation des incidents :** Automatiser la vérification des alertes entrantes en croisant les domaines suspects avec les analyses de phishing de Criminal IP avant toute intervention humaine.

---
[Source](https://www.bleepingcomputer.com/news/security/turning-indicators-into-intelligence-in-opencti-with-criminal-ip/){:target="_blank"}
