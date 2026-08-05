---
title: 'COLDCARD security audit phishing attack installs remote access tool'
date: 2026-08-05
permalink: /posts/2026/08/05/coldcard-security-audit-phishing-attack-installs-remote-access-tool/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de phishing visant les utilisateurs de COLDCARD : Installation de logiciels d'accès à distance

Une campagne de phishing sophistiquée cible les détenteurs de portefeuilles de cryptomonnaies COLDCARD en exploitant le climat d'inquiétude lié à un récent vol massif de Bitcoin (environ 88,6 millions de dollars). Les attaquants se font passer pour le support officiel afin d'inciter les utilisateurs à télécharger un prétendu « outil d'audit de sécurité ».

**Points clés :**
*   **Mode opératoire :** Envoi d'e-mails frauduleux incitant à vérifier l'intégrité du matériel via un faux site web (`coldcardcompliance.com`).
*   **Ingénierie sociale :** Présence d'un chat en direct où des opérateurs humains manipulent les victimes pour qu'elles autorisent l'installation de logiciels.
*   **Charge utile (Payload) :** Le téléchargement d'un fichier `.bat` installe en arrière-plan **ScreenConnect**, un outil légitime de prise de contrôle à distance, utilisé ici à des fins malveillantes. Un faux pilote d'imprimante DocuSign est également installé pour servir de leurre.
*   **Risques :** Accès distant total à la machine, vol de données, exfiltration de cryptomonnaies ou déploiement de ransomwares.

**Vulnérabilités associées :**
*   L'attaque ne repose pas sur une faille logicielle spécifique (CVE), mais sur une exploitation de la confiance de l'utilisateur (phishing) et l'élévation de privilèges via l'exécution de scripts (`PowerShell`/`certutil`) avec des droits d'administrateur.
*   La faille initiale ayant motivé le vol de 88,6 millions de dollars est une vulnérabilité dans le générateur de nombres aléatoires (RNG) des appareils COLDCARD.

**Recommandations :**
*   **Vigilance sur les communications :** Ne jamais télécharger d'outils de "diagnostic" ou de "mise à jour" depuis des liens reçus par e-mail ou des sites tiers, même s'ils semblent officiels.
*   **Vérification des sources :** Seules les annonces publiées sur le site officiel de COLDCARD (et confirmées par ses canaux de communication officiels) doivent être prises en compte.
*   **Prudence avec les privilèges :** Refuser systématiquement toute demande d'élévation de privilèges (UAC) provenant d'un logiciel dont la source n'est pas vérifiée ou qui n'est pas strictement nécessaire.
*   **Analyse des fichiers :** En cas de doute, scanner les fichiers téléchargés via des plateformes comme VirusTotal avant toute exécution.

---
[Source](https://www.bleepingcomputer.com/news/security/coldcard-security-audit-phishing-attack-installs-remote-access-tool/){:target="_blank"}
