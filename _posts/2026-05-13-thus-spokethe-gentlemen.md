---
title: 'Thus Spoke…The Gentlemen'
date: 2026-05-13
permalink: /posts/2026/05/13/thus-spokethe-gentlemen/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse du groupe de ransomware "The Gentlemen"

Le groupe **The Gentlemen**, apparu mi-2025, est devenu l'une des opérations de "Ransomware-as-a-Service" (RaaS) les plus actives, comptabilisant plus de 330 victimes au cours des cinq premiers mois de 2026. Une fuite de leur base de données interne ("Rocket") et de leurs conversations a levé le voile sur leur structure opérationnelle hautement organisée.

**Points clés :**
*   **Structure :** Une équipe restreinte d'environ 9 opérateurs principaux, sous la direction de `zeta88` (alias `hastalamuerte`), qui gère l'infrastructure, le développement du locker et les négociations.
*   **Modèle :** Un programme d'affiliation avec un partage de revenus de 90/10, impliquant au moins 8 affiliés identifiés par leur TOX ID.
*   **Mode opératoire :** Utilisation d'accès initiaux via des équipements périphériques (VPN, pare-feu Fortinet/Cisco), suivis d'une escalade de privilèges, de mouvements latéraux et de l'utilisation intensive d'outils de "red-teaming".
*   **Tactiques de pression :** Réutilisation de données volées lors de précédentes attaques pour enrichir et faciliter de nouvelles intrusions, avec une stratégie de double extorsion.

**Vulnérabilités activement exploitées ou suivies :**
*   **CVE-2024-55591 :** Interface de gestion FortiOS.
*   **CVE-2025-32433 :** Vulnérabilité SSH (contexte Erlang/Cisco).
*   **CVE-2025-33073 :** Problèmes de réflexion/relais NTLM.
*   *Techniques additionnelles :* Abus de services MSI (`RegPwn`), exploitation des infrastructures Veeam/iDRAC, et manipulation des logs/ETW pour contourner les solutions EDR/AV.

**Recommandations de sécurité :**
*   **Durcissement des accès :** Sécuriser strictement tous les équipements exposés sur Internet (VPN, pare-feu, passerelles OWA/M365) et appliquer les correctifs pour les vulnérabilités susmentionnées.
*   **Protection contre le relais NTLM :** Auditer et limiter les risques de relais NTLM (notamment via la désactivation de l'authentification NTLM là où elle n'est pas requise et l'utilisation de SMB Signing).
*   **Surveillance EDR :** Détecter les tentatives de désactivation des services de sécurité (EDR/AV) et surveiller les outils suspects utilisés pour la reconnaissance (ex: `NetExec`, `RelayKing`, `PrivHound`).
*   **Gestion des identités :** Renforcer la sécurité des comptes administrateurs et limiter l'utilisation de comptes à haut privilège sur les machines endpoints pour contrer les mouvements latéraux.
*   **Veille opérationnelle :** Surveiller les communications basées sur des IDs de messagerie TOX et les schémas d'exfiltration de données vers des infrastructures NAS ou cloud non autorisées.

---
[Source](https://research.checkpoint.com/2026/thus-spoke-the-gentlemen/){:target="_blank"}
