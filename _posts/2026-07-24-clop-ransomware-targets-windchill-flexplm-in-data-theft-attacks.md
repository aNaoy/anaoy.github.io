---
title: 'Clop ransomware targets Windchill, FlexPLM in data theft attacks'
date: 2026-07-24
permalink: /posts/2026/07/24/clop-ransomware-targets-windchill-flexplm-in-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'extorsion Clop visant les plateformes PTC Windchill et FlexPLM

Le groupe de ransomware Clop mène actuellement une campagne d'exfiltration de données ciblant les instances exposées sur Internet des solutions de gestion du cycle de vie des produits (PLM) **PTC Windchill** et **FlexPLM**. Les attaquants utilisent des *webshells* JSP pour prendre le contrôle des serveurs et dérober des données sensibles avant de contacter les employés des entreprises visées pour réclamer une rançon.

#### Points clés
*   **Mode opératoire :** Exploitation de serveurs vulnérables pour exécuter du code à distance, suivie d'une phase d'exfiltration massive de données industrielles et techniques.
*   **Tactiques d'extorsion :** Utilisation de comptes email compromis pour envoyer des messages de menace à un large nombre d'employés au sein des organisations ciblées.
*   **Impact :** Les secteurs de l'aérospatiale, de la défense, de l'automobile et de la technologie médicale sont particulièrement exposés.

#### Vulnérabilité exploitée
*   **CVE-2026-12569 :** Vulnérabilité critique de désérialisation non sécurisée (score CVSS 9.3). Elle permet l'exécution de code à distance (RCE) non authentifiée et le déploiement de *webshells*.

#### Recommandations
*   **Correctifs :** Appliquer immédiatement les patchs de sécurité fournis par PTC.
*   **Isolement :** Placer les instances de Windchill et FlexPLM derrière des VPN ou des passerelles d'accès sécurisées (Zero Trust).
*   **Réponse aux incidents :** En cas de suspicion de compromission, isoler les serveurs affectés, collecter les preuves forensiques et procéder à une rotation complète de toutes les identifiants exposés avant toute remise en service.
*   **Surveillance :** Rechercher les indicateurs de compromission (IOC) dans les environnements exposés et surveiller les journaux d'accès pour détecter toute activité inhabituelle.

---
[Source](https://www.bleepingcomputer.com/news/security/clop-ransomware-targets-windchill-flexplm-in-data-theft-attacks/){:target="_blank"}
