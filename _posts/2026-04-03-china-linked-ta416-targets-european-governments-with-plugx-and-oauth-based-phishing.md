---
title: 'China-Linked TA416 Targets European Governments with PlugX and OAuth-Based Phishing'
date: 2026-04-03
permalink: /posts/2026/04/03/china-linked-ta416-targets-european-governments-with-plugx-and-oauth-based-phishing/
tags:
- veille-cyber
- hackernews
---
### Espionnage cybernétique : TA416 cible les gouvernements européens

Le groupe de menace TA416 (également associé à Mustang Panda et RedDelta) a repris ses activités d'espionnage contre les institutions gouvernementales et diplomatiques européennes, ainsi qu'au Moyen-Orient. Ce groupe, lié à la Chine, fait preuve d'une grande agilité en adaptant constamment ses vecteurs d'attaque pour contourner les défenses de sécurité.

**Points clés :**
*   **Objectifs :** Missions diplomatiques liées à l'UE et à l'OTAN, ainsi que des entités gouvernementales au Moyen-Orient.
*   **Techniques d'infection :** Utilisation de "web bugs" (pixels espions) pour la reconnaissance, exploitation de redirections OAuth via Microsoft Entra ID, et envoi d'archives malveillantes hébergées sur des services légitimes (Google Drive, SharePoint, Azure Blob Storage).
*   **Déploiement de charge utile :** Utilisation de fichiers projet MSBuild (.csproj) pour télécharger et exécuter le backdoor **PlugX** via une technique de *DLL side-loading*.
*   **Persistance :** Les opérations sont conçues pour un accès longue durée, avec une capacité d'hibernation prolongée dans les réseaux compromis.

**Vulnérabilités mentionnées :**
L'exploitation d'infrastructures exposées sur Internet reste un vecteur majeur pour les cyber-opérations chinoises, notamment via des vulnérabilités critiques comme :
*   **CVE-2025-31324**
*   **CVE-2025-0994**

**Recommandations :**
*   **Surveillance OAuth :** Auditer et restreindre l'utilisation des applications tierces Microsoft Entra ID pour prévenir les abus de redirection URL.
*   **Gestion des exécutables :** Limiter l'exécution de binaires système légitimes (comme MSBuild) par des utilisateurs finaux ou des processus non autorisés, afin d'empêcher le *DLL side-loading*.
*   **Filtrage e-mail :** Mettre en place des solutions capables de détecter les "web bugs" et de bloquer les liens pointant vers des services cloud tiers détournés pour l'hébergement de malwares.
*   **Analyse comportementale :** Surveiller les comportements anormaux au sein du réseau, particulièrement après une intrusion initiale, pour détecter les tentatives de persistance à long terme.

---
[Source](https://thehackernews.com/2026/04/china-linked-ta416-targets-european.html){:target="_blank"}
