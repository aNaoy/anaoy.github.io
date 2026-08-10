---
title: 'China-Linked Hackers Deploy New StormEncryptor Ransomware, Likely via N-central Flaw'
date: 2026-08-10
permalink: /posts/2026/08/10/china-linked-hackers-deploy-new-stormencryptor-ransomware-likely-via-n-central-flaw/
tags:
- veille-cyber
- hackernews
---
### Émergence du ransomware StormEncryptor par le groupe Storm-1175

Le groupe cybercriminel Storm-1175, lié à la Chine, a diversifié son arsenal en abandonnant le ransomware Medusa au profit d'une nouvelle souche nommée **StormEncryptor**. Ce groupe se distingue par sa capacité à exploiter rapidement des vulnérabilités critiques, souvent peu après leur divulgation, pour mener des attaques fulgurantes allant de l'intrusion initiale à l'exfiltration de données en quelques jours.

**Points clés :**
*   **Mode opératoire :** Utilisation d'outils d'administration à distance (AnyDesk, SimpleHelp) et de logiciels d'analyse réseau pour le mouvement latéral, complété par l'extraction d'identifiants via Mimikatz (vidage LSASS).
*   **StormEncryptor :** Développé en C++, ce ransomware ajoute l'extension `.encrypted` aux fichiers chiffrés et dépose une demande de rançon intitulée `!!!README_FIRST!!!.txt`.
*   **Stratégie :** Le groupe capitalise sur le délai entre la publication d'un correctif et son déploiement effectif par les organisations pour compromettre les systèmes exposés sur Internet.

**Vulnérabilités exploitées :**
*   **CVE-2026-18577 :** Vulnérabilité critique dans N-able N-central, utilisée pour le contournement d'authentification et la prise de contrôle de comptes (il s'agit d'un contournement du correctif pour la **CVE-2026-18556**).
*   *Note :* Le groupe possède un historique d'exploitation de vulnérabilités dans Mirth Connect, ConnectWise ScreenConnect, JetBrains TeamCity, Fortinet FortiClient EMS et Fortra GoAnywhere.

**Recommandations :**
*   **Application immédiate des correctifs :** La rapidité d'exécution du groupe impose une mise à jour prioritaire des systèmes, en particulier pour les produits N-able N-central.
*   **Surveillance accrue :** Porter une attention particulière aux outils RMM (Remote Monitoring and Management) et aux scanners réseau suspects au sein du parc informatique.
*   **Protection des identifiants :** Mettre en place des mesures contre le dump de mémoire LSASS pour limiter la progression des attaquants après une compromission initiale.

---
[Source](https://thehackernews.com/2026/08/china-linked-hackers-deploy-new.html){:target="_blank"}
