---
title: 'Microsoft warns of surge in ACR Stealer attacks on customers'
date: 2026-07-18
permalink: /posts/2026/07/18/microsoft-warns-of-surge-in-acr-stealer-attacks-on-customers/
tags:
- veille-cyber
- bleepingcomp
---
### Recrudescence des attaques par le logiciel malveillant ACR Stealer

Microsoft a alerté sur une augmentation significative des attaques utilisant **ACR Stealer**, un malware proposé sous forme de service (MaaS) — supposé être une évolution de l'Amatera Stealer — ciblant les entreprises pour dérober des identifiants, des jetons d'authentification et des documents confidentiels.

**Points clés :**
*   **Méthodologie :** Utilisation intensive de la technique d'ingénierie sociale "ClickFix" incitant les utilisateurs à exécuter des commandes malveillantes sous prétexte de résolution d'erreur.
*   **Chaînes d'infection :**
    *   **Vecteur WebDAV :** Utilisation de serveurs WebDAV distants pour charger des DLL malveillantes via `rundll32.exe`.
    *   **Vecteur MSHTA :** Exploitation de l'utilitaire `mshta.exe` pour récupérer et exécuter des scripts PowerShell obfusqués.
*   **Techniques d'évasion :** Utilisation de stéganographie (images JPEG), manipulation d'horodatages, effacement des historiques PowerShell et recours à la technologie « EtherHiding » (utilisation de blockchains publiques pour masquer les adresses C2).
*   **Objectifs :** Vol de données de navigation (Chrome, Edge), accès aux dossiers locaux (Desktop, Downloads) et exfiltration de documents sensibles synchronisés via OneDrive et SharePoint.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus détourné de fonctionnalités système légitimes (**Living-off-the-Land**) :
*   Abus de **WebDAV** pour le transfert de fichiers.
*   Utilisation détournée de **MSHTA**, **PowerShell**, **Python** et **rundll32.exe**.
*   Exploitation du **DPAPI** (Windows Data Protection API) pour déchiffrer les données de navigation.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à ne jamais copier ni exécuter de commandes dans des interpréteurs (PowerShell, CMD) à la suite d'une demande sur une page web.
*   **Contrôle des applications :** Restreindre strictement l'exécution de scripts ou de binaires (`powershell.exe`, `python.exe`, `mshta.exe`, `rundll32.exe`) depuis des répertoires accessibles en écriture par l'utilisateur ou depuis des sources distantes.
*   **Filtrage réseau :** Bloquer les connexions vers les domaines à faible réputation ou nouvellement créés et limiter l'accès aux ressources en ligne non nécessaires aux opérations métier.
*   **Surveillance :** Surveiller la création de tâches planifiées suspectes et les activités anormales liées aux dossiers WebDAV.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-warns-of-surge-in-acr-stealer-attacks-on-customers/){:target="_blank"}
