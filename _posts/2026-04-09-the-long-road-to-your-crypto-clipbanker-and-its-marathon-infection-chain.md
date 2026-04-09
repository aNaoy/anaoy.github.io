---
title: 'The long road to your crypto: ClipBanker and its marathon infection chain'
date: 2026-04-09
permalink: /posts/2026/04/09/the-long-road-to-your-crypto-clipbanker-and-its-marathon-infection-chain/
tags:
- veille-cyber
- securelist
---
### Analyse de la campagne ClipBanker : Un piège par infection séquentielle

Cette campagne malveillante cible les utilisateurs recherchant des logiciels gratuits, notamment le logiciel "Proxifier". Les attaquants utilisent des référentiels GitHub frauduleux pour distribuer un installeur piégé contenant une version légitime du logiciel accompagnée d'un malware de type "ClipBanker".

**Points clés de l'infection :**
*   **Vecteur initial :** Optimisation du référencement (SEO) sur GitHub pour attirer les utilisateurs recherchant des versions gratuites de logiciels payants.
*   **Chaîne d'infection "marathon" :** Utilisation de multiples couches d'injection de processus (process hollowing) et de scripts PowerShell hautement obfusqués.
*   **Techniques "Fileless" :** Le malware minimise son empreinte sur le disque en exécutant des charges utiles directement en mémoire vive via des processus système légitimes (`conhost.exe`, `fontdrvhost.exe`).
*   **Objectif final :** Surveillance constante du presse-papier pour intercepter des adresses de portefeuilles cryptographiques et les remplacer par celles des attaquants lors des transactions.

**Vulnérabilités exploitées :**
*   **Absence de CVE spécifique :** L'attaque repose sur l'ingénierie sociale (téléchargement de logiciels piratés) et l'abus de fonctionnalités système légitimes (PowerShell, `PSObject`, injections mémoire) plutôt que sur l'exploitation de failles logicielles documentées.
*   **Désactivation des mesures de sécurité :** Le malware tente activement d'ajouter des exclusions dans Microsoft Defender pour masquer ses activités et persister dans le registre système (`HKLM\SOFTWARE\System::Config`).

**Recommandations :**
*   **Sources officielles uniquement :** Téléchargez systématiquement vos logiciels depuis les sites web officiels des éditeurs. Évitez les plateformes tierces, les liens GitHub non vérifiés ou les sites proposant des clés d'activation ("cracks").
*   **Vigilance sur le presse-papier :** Avant de valider une transaction en cryptomonnaie, vérifiez systématiquement que l'adresse de destination collée correspond bien à celle prévue initialement.
*   **Protection proactive :** Utilisez une solution de sécurité réputée capable de détecter les comportements suspects et les scripts malveillants avant leur exécution, plutôt que de devoir nettoyer un système déjà compromis.
*   **Gestion des privilèges :** Limitez l'exécution de scripts PowerShell non signés et surveillez les modifications suspectes des clés de registre ou l'ajout d'exclusions dans votre antivirus.

---
[Source](https://securelist.com/clipbanker-malware-distributed-via-trojanized-proxifier/119341/){:target="_blank"}
