---
title: 'Telus Digital confirms breach after hacker claims 1 petabyte data theft'
date: 2026-03-12
permalink: /posts/2026/03/12/telus-digital-confirms-breach-after-hacker-claims-1-petabyte-data-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Violation massive chez Telus Digital : près d'un pétaoctet de données exposé

Le géant de l'externalisation des services (BPO) Telus Digital a confirmé une cyberattaque majeure orchestrée par le groupe de cybercriminels **ShinyHunters**. Les attaquants affirment avoir exfiltré près d'un pétaoctet (1 Po) de données sensibles, incluant des informations relatives à de nombreuses entreprises clientes, ainsi que des données internes de la division télécom de Telus.

**Points clés :**
*   **Vol de données massif :** Les données compromises concerneraient des enregistrements d'appels, du code source, des informations financières, des données Salesforce et des vérifications d'antécédents (FBI).
*   **Méthode d'extorsion :** Les pirates ont tenté d'extorquer 65 millions de dollars à Telus en échange du non-divulgation des données ; Telus a refusé toute négociation.
*   **Impact transverse :** En tant que fournisseur BPO, Telus a potentiellement exposé des données appartenant à 28 autres grandes entreprises clientes.

**Vulnérabilités exploitées :**
*   **Fuite de secrets (Credential Stuffing/Leakage) :** Les attaquants ont récupéré des identifiants Google Cloud Platform (GCP) exposés dans une précédente fuite de données (incident Salesloft Drift).
*   **Mouvement latéral :** Utilisation de l'outil *Trufflehog* pour scanner les données volées à la recherche de secrets supplémentaires, permettant ainsi de pivoter vers d'autres systèmes critiques de l'entreprise.
*   **Pas de CVE spécifique :** L'incident résulte d'une mauvaise gestion de la rotation des secrets et d'une exposition involontaire d'identifiants dans des bases de données tierces.

**Recommandations :**
*   **Gestion stricte des secrets :** Éviter impérativement le stockage en clair ou non protégé de clés API, de tokens d'authentification ou d'identifiants cloud dans des référentiels de code ou des instances SaaS.
*   **Audit et rotation proactive :** Réaliser régulièrement des audits pour détecter les secrets exposés (via des outils comme TruffleHog) et automatiser la rotation des identifiants cloud.
*   **Sécurisation des accès SaaS/Cloud :** Mettre en œuvre le principe du moindre privilège pour les comptes de service et renforcer l'authentification avec des méthodes résistantes au phishing (clés matérielles FIDO2/WebAuthn), particulièrement pour les services critiques connectés (Salesforce, Google Cloud, Microsoft Entra).
*   **Surveillance active :** Surveiller les accès aux instances BigQuery et aux environnements cloud pour détecter des comportements anormaux ou des volumes d'exfiltration massifs.

---
[Source](https://www.bleepingcomputer.com/news/security/telus-digital-confirms-breach-after-hacker-claims-1-petabyte-data-theft/){:target="_blank"}
