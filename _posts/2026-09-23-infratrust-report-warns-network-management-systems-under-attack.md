---
title: 'InfraTrust report warns network management systems under attack'
date: 2026-09-23
permalink: /posts/2026/09/23/infratrust-report-warns-network-management-systems-under-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Menace croissante sur les systèmes de gestion d'infrastructure

Le rapport *InfraTrust Pulse* de septembre 2026 met en lumière une tendance préoccupante : les attaquants ciblent désormais prioritairement les plateformes de gestion et d'administration (consoles de configuration, orchestrateurs). Ces outils sont devenus des cibles de haute valeur car ils centralisent les identifiants et offrent un accès total à l'ensemble du réseau. Entre fin août et mi-septembre, 1 699 vulnérabilités ont été identifiées, dont 42 critiques, touchant de nombreux constructeurs majeurs.

**Points clés :**
*   **Ciblage des consoles d'administration :** Les outils de contrôle (Cisco, SonicWall, HPE, Dell, NVIDIA, etc.) sont massivement attaqués pour compromettre l'infrastructure en profondeur.
*   **Exploitation active :** Plusieurs vulnérabilités critiques sont exploitées par des gangs de ransomwares et des acteurs étatiques avant même ou peu après leur divulgation.
*   **Complexité de la chaîne d'approvisionnement :** Une seule faille dans un composant tiers (ex: Linux "CopyFail") peut engendrer des dizaines de correctifs éparpillés chez différents constructeurs, multipliant la charge de travail des administrateurs.
*   **Risques au niveau du firmware :** Des vulnérabilités de type *Secure Boot bypass* permettent l'exécution de code non signé dès le démarrage du système.

**Vulnérabilités majeures identifiées :**
*   **Cisco Secure Firewall Management Center (FMC) :** 
    *   **CVE-2026-20079 & CVE-2026-20316 :** Chaînage de failles permettant une exécution de code à distance (RCE) en tant que root.
*   **Cisco Identity Services Engine (ISE) :**
    *   **CVE-2026-76460 :** Contournement d'authentification critique (CVSS 10.0) permettant l'exécution de commandes root via API.
*   **SonicWall SMA 1000 :** 
    *   **CVE-2026-83548 & CVE-2026-83549 :** Chaînage de SSRF et injection de commandes OS pour RCE.
*   **Check Point VPN/Management :**
    *   **CVE-2026-85102, CVE-2026-85103, CVE-2026-91843 :** Failles critiques permettant l'exécution de code à distance sans authentification.
*   **Composant Linux (CopyFail) :** 
    *   **CVE-2026-31431 :** Escalade de privilèges exploitée sur 19 produits différents.

**Recommandations :**
*   **Renforcement immédiat :** Traiter les plateformes d'administration réseau comme des systèmes hautement sensibles. Appliquer les correctifs de sécurité en priorité absolue.
*   **Accès restreint :** En l'absence de correctifs (ou pour les réduire), restreindre strictement l'accès aux interfaces de gestion via des listes de contrôle d'accès (ACL) réseau.
*   **Remédiation drastique :** Pour les systèmes déjà compromis, privilégier le re-déploiement complet ou la ré-installation à partir d'images propres plutôt qu'une tentative de nettoyage local.
*   **Surveillance accrue :** Rechercher les indicateurs de compromission (IoC) sur les outils d'administration et auditer régulièrement les configurations du *Secure Boot* et des paramètres de démarrage UEFI.

---
[Source](https://www.bleepingcomputer.com/news/security/infratrust-report-warns-network-management-systems-under-attack/){:target="_blank"}
