---
title: 'Analysis of a Year of Files Uploaded to DShield Sensors, (Wed, May 27th)'
date: 2026-05-29
permalink: /posts/2026/05/29/analysis-of-a-year-of-files-uploaded-to-dshield-sensors-wed-may-27th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des tendances des logiciels malveillants via les capteurs DShield

Une analyse sur un an des données collectées par les capteurs DShield (Cowrie) révèle une activité fluctuante, avec un pic de téléchargements de fichiers malveillants durant l'hiver (décembre 2025 à février 2026), suivi d'une baisse significative à partir de mars 2026. Cette étude s'appuie sur l'enrichissement des données via VirusTotal et leur visualisation au sein d'une pile SIEM.

**Points clés :**
* **Types de fichiers identifiés :** Les menaces observées se répartissent principalement entre les formats ELF, scripts Shell, PowerShell, HTML, texte, fichiers batch DOS, JavaScript et fichiers non identifiés.
* **Méthodologie :** L'utilisation de requêtes ES|QL dans Kibana permet de corréler les hashes des fichiers, leurs types et les noms des logiciels malveillants associés à partir des logs des capteurs.
* **Outils d'enrichissement :** Le processus repose sur des scripts Python automatisés (`cowrie_vt.sh` et `cowrie_malware_enrichment.py`) pour enrichir quotidiennement les fichiers capturés par les honeypots.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifiques, car il se concentre sur l'analyse statistique des types de fichiers malveillants rencontrés sur les réseaux, plutôt que sur l'exploitation de failles logicielles précises.

**Recommandations :**
* **Surveillance active :** Déployer des capteurs honeypot pour identifier les vecteurs d'attaque émergents et les types de fichiers malveillants en circulation.
* **Centralisation SIEM :** Utiliser des solutions comme le DShield SIEM pour corréler les données des capteurs avec des services de réputation (type VirusTotal) afin de filtrer et prioriser les menaces.
* **Automatisation :** Exploiter les scripts d'enrichissement fournis pour automatiser la classification des fichiers malveillants et améliorer la réactivité des équipes de sécurité face aux nouvelles signatures.

---
[Source](https://isc.sans.edu/diary/rss/33026){:target="_blank"}
