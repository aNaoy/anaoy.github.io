---
title: 'Microsoft Restores Some GitHub Repos, Keeps Others Offline as Miasma Probe Continues'
date: 2026-06-09
permalink: /posts/2026/06/09/microsoft-restores-some-github-repos-keeps-others-offline-as-miasma-probe-continues/
tags:
- veille-cyber
- hackernews
---
### Campagne de compromission de la supply chain : L'incident "Miasma"

Microsoft a temporairement suspendu l'accès à 73 de ses dépôts GitHub suite à la découverte d'une campagne de compromission visant à injecter un logiciel voleur d'informations (*infostealer*) dans ses projets open-source. Les attaquants, regroupés sous des noms de campagnes tels que "Miasma", "Hades" et "Mini Shai-Hulud", ciblent activement les développeurs et les environnements CI/CD.

**Points clés :**
* **Ciblage :** En plus des projets Microsoft (ex: *durabletask*), la campagne vise des bibliothèques de bio-informatique et des paquets liés à l'intelligence artificielle (MCP - Model Context Protocol).
* **Méthodes d'exécution :** Les malwares utilisent des hooks de démarrage `.pth` et des extensions natives `.abi3.so` pour s'exécuter automatiquement lors de l'importation d'un paquet.
* **Évasion :** Les attaquants utilisent des injections de prompts adverses pour tromper les scanners de sécurité basés sur l'IA et séparent le chargeur de la charge utile pour contourner l'analyse statique.
* **Impact :** Vol de secrets et d'identifiants sur les postes de travail des développeurs et dans les pipelines d'intégration continue.

**Vulnérabilités :**
L'attaque repose sur l'empoisonnement de paquets (typosquatting) et la manipulation de mécanismes d'exécution automatique natifs de Python (CVE non spécifiées, exploitant des fonctionnalités légitimes détournées). Les paquets compromis incluent notamment : *rsquests*, *tlask*, *rlask*, *langchain-core-mcp* et divers outils de bio-informatique (ex: *gpsea*, *pyphetools*).

**Recommandations :**
* **Vérification :** Auditer les dépendances de projet, particulièrement celles liées à l'IA ou à la bio-informatique, en recherchant des paquets suspects.
* **Sécurisation CI/CD :** Isoler les environnements de build et surveiller les accès suspects aux secrets.
* **Analyse :** Se méfier des paquets aux noms proches des bibliothèques standards (typosquatting) et privilégier l'épinglage strict des versions (hashes).
* **Suivi :** Les utilisateurs ayant téléchargé des contenus depuis les dépôts impactés doivent surveiller leurs canaux de support Microsoft pour d'éventuelles instructions de remédiation.

---
[Source](https://thehackernews.com/2026/06/microsoft-restores-some-github-repos.html){:target="_blank"}
