---
title: 'Claimed Bug Bounty Hunter Likely Used LLM to Build PhantomRaven npm Stealer'
date: 2026-09-18
permalink: /posts/2026/09/18/claimed-bug-bounty-hunter-likely-used-llm-to-build-phantomraven-npm-stealer/
tags:
- veille-cyber
- hackernews
---
### L'émergence de PhantomRaven : un malware assisté par IA pour infiltrer la supply chain

Un acteur malveillant, se présentant comme un chasseur de primes (bug bounty), utilise le logiciel malveillant **PhantomRaven** pour compromettre des environnements de développement. Ce malware, diffusé via des paquets npm piégés, a probablement été généré à l'aide d'un grand modèle de langage (LLM), une tendance qui accélère le développement de cybermenaces.

**Points clés :**
*   **Mode opératoire :** L'attaquant utilise des techniques de *typosquatting* et de *slopsquatting* pour publier des bibliothèques npm malveillantes. Une fois installées, elles téléchargent une dépendance dynamique distante (RDD) pour échapper à la détection.
*   **Objectif inhabituel :** Contrairement aux cybercriminels classiques, cet acteur utilise les données volées (clés CI/CD, identifiants GitHub, variables d'environnement) pour identifier des vulnérabilités au sein d'entreprises et toucher des primes de programmes de *bug bounty*.
*   **Portée :** Plus de 100 paquets ont été identifiés, avec des tentatives d'extension vers l'écosystème Python (PyPI). L'activité remonte à novembre 2022.

**Vulnérabilités exploitées :**
*   L'attaque repose sur la compromission de la chaîne d'approvisionnement logicielle via l'exécution de scripts (`preinstall`) dans les paquets npm.
*   Aucune CVE spécifique n'est associée, car il s'agit d'une utilisation abusive de fonctionnalités légitimes de gestionnaire de paquets couplée à une ingénierie sociale/typosquatting.

**Recommandations :**
*   **Vérification des dépendances :** Auditer strictement les paquets npm ou PyPI ajoutés aux projets, en vérifiant leur popularité, leur intégrité et leur auteur avant toute installation.
*   **Isolement CI/CD :** Restreindre les privilèges des environnements de CI/CD et éviter d'y stocker des secrets sensibles qui ne sont pas strictement nécessaires à l'exécution des builds.
*   **Surveillance réseau :** Surveiller les comportements suspects liés à l'exécution de scripts (`preinstall` ou `postinstall`) et le téléchargement inattendu de dépendances distantes par les applications.
*   **Analyse de configuration :** Scanner régulièrement les variables d'environnement et les configurations Git/npm sur les postes des développeurs pour détecter toute fuite d'informations.

---
[Source](https://thehackernews.com/2026/09/claimed-bug-bounty-hunter-likely-used.html){:target="_blank"}
