---
title: 'ClickFix Lures Deploy ChainScript RAT Using Polygon to Rotate C2 Infrastructure'
date: 2026-09-21
permalink: /posts/2026/09/21/clickfix-lures-deploy-chainscript-rat-using-polygon-to-rotate-c2-infrastructure/
tags:
- veille-cyber
- hackernews
---
### Propagation de ChainScript via des leurres ClickFix et la blockchain

Les cyberattaquants déploient désormais **ChainScript**, un cheval de Troie d'accès à distance (RAT) basé sur Node.js, en utilisant des techniques d'ingénierie sociale de type « ClickFix ». Ce malware se dissimule sous l'apparence de logiciels légitimes (Spotify, Zoom, Microsoft Teams) pour infiltrer les systèmes Windows.

**Points clés :**
*   **Infrastructure décentralisée :** Le malware utilise des contrats intelligents sur la blockchain Polygon pour localiser dynamiquement son serveur de commande et contrôle (C2), rendant la détection et le démantèlement par les autorités extrêmement complexes.
*   **Capacités du RAT :** ChainScript permet une prise de contrôle totale : exécution de commandes CMD/PowerShell, capture d'écran, vol de cryptomonnaies (extensions de navigateur et portefeuilles) et exécution de scripts JavaScript distants.
*   **Persistance :** Le malware s'installe via des tâches planifiées et des clés de registre, assurant son maintien sur la machine compromise.
*   **Menace étendue :** Parallèlement, des campagnes comme *PasteSwitch* exploitent des comptes compromis (ex: HBO Max sur Reddit) pour diffuser des malwares (MacSync, Atomic Stealer) via des leurres ClickFix visant à la fois Windows et macOS.

**Vulnérabilités :**
L'attaque ne repose pas sur une vulnérabilité logicielle spécifique (CVE), mais sur l'exploitation de la confiance des utilisateurs par des méthodes de **typosquatting**, d'usurpation d'identité sur les réseaux sociaux et de manipulation de l'utilisateur (inviter la victime à copier-coller des commandes malveillantes dans le terminal ou à exécuter des installateurs MSI piégés).

**Recommandations :**
*   **Sensibilisation :** Se méfier systématiquement des instructions demandant de copier/coller des commandes dans un terminal ou d'exécuter des scripts suite à une interaction sur une page web.
*   **Contrôle des sources :** Télécharger exclusivement les logiciels depuis les sites officiels des éditeurs et éviter les publicités sur les réseaux sociaux ou les moteurs de recherche.
*   **Sécurisation des terminaux :** Utiliser des solutions EDR (Endpoint Detection and Response) capables de détecter des comportements anormaux, comme l'exécution de scripts PowerShell dissimulés ou des activités réseau inhabituelles.
*   **Gestion des accès :** Appliquer le principe du moindre privilège pour limiter l'impact en cas d'exécution d'un code malveillant sur un poste de travail.

---
[Source](https://thehackernews.com/2026/09/clickfix-lures-deploy-chainscript-rat.html){:target="_blank"}
