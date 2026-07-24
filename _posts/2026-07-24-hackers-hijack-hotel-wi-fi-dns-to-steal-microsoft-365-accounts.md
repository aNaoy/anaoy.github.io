---
title: 'Hackers hijack hotel Wi-Fi DNS to steal Microsoft 365 accounts'
date: 2026-07-24
permalink: /posts/2026/07/24/hackers-hijack-hotel-wi-fi-dns-to-steal-microsoft-365-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Piratage DNS dans les hôtels : vol de comptes Microsoft 365

Des cybercriminels compromettent les passerelles Wi-Fi d'hôtels et de centres de conférence pour rediriger les utilisateurs vers de fausses pages de connexion Microsoft 365. Cette campagne, potentiellement liée au groupe APT28, cible les voyageurs d'affaires quel que soit leur secteur d'activité.

**Points clés :**
*   **Méthode :** Les attaquants prennent le contrôle de l'administration des routeurs Wi-Fi (via des accès SSH, SNMP ou web mal protégés) pour modifier les paramètres DNS.
*   **Phishing et OAuth :** En plus des formulaires de connexion classiques, les attaquants utilisent le flux d'authentification par code d'appareil (*Device Code flow*) pour inciter les victimes à autoriser une session, permettant ainsi de générer un jeton OAuth légitime et de contourner l'authentification multifacteur (MFA).
*   **Propagation :** Une tentative d'abus du protocole WPAD (Web Proxy Auto-Discovery) est également observée pour rediriger le trafic via un proxy malveillant.
*   **Inopérance du DNS public :** L'utilisation de serveurs DNS externes (comme 8.8.8.8) ne protège pas contre cette attaque, car la passerelle falsifie les requêtes avant qu'elles ne quittent le réseau local.

**Vulnérabilités :**
*   Absence de CVE spécifique : L'attaque repose sur l'exploitation de configurations faibles ou d'interfaces d'administration exposées (SSH/SNMP/Web) sur le matériel réseau.

**Recommandations :**
*   **VPN :** Utiliser systématiquement un VPN en mode "full-tunnel".
*   **Configuration réseau :** Activer le DNS chiffré en mode "strict" sur les postes clients.
*   **Paramètres Microsoft Entra ID :** Désactiver le flux d'authentification par code d'appareil (*Device Code authentication*) s'il n'est pas nécessaire.
*   **Système :** Désactiver le protocole WPAD sur les terminaux Windows.
*   **Surveillance :** Analyser les journaux réseau pour détecter des redirections suspectes ou des comportements anormaux.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hijack-hotel-wi-fi-dns-to-steal-microsoft-365-accounts/){:target="_blank"}
