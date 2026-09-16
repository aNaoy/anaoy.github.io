---
title: 'NightEagle targets Russian companies'
date: 2026-09-16
permalink: /posts/2026/09/16/nighteagle-targets-russian-companies/
tags:
- veille-cyber
- securelist
---
### Expansion des activités du groupe APT NightEagle vers la Russie

Le groupe APT NightEagle (APT-Q-95) a étendu ses opérations, initialement concentrées en Asie, vers des organisations en Russie. Cette campagne repose sur l'utilisation de justificatifs d'identité compromis pour accéder aux VPN d'entreprise, suivie par le déploiement du backdoor *GhostContainer* sur des serveurs Microsoft Exchange.

**Points clés :**
*   **Accès initial :** Utilisation de comptes VPN valides, souvent via des tunnels Cloudflare WARP ou des infrastructures virtuelles européennes.
*   **Persistence et outils :** Le groupe utilise des outils légitimes détournés (Microsoft dev tunnels, *rdp2tcp*) et des exécutables maquillés (nommés *adobe_32.exe*, *1cbroker.exe*, etc.) hébergés sur GitHub pour le mouvement latéral et le tunneling.
*   **Mouvement latéral :** Exploitation d'Active Directory, incluant l'utilisation de la technique DCSync pour usurper l'identité du contrôleur de domaine et extraire des secrets.

**Vulnérabilités exploitées :**
*   **CVE-2020-0688 :** Utilisée dans les composants de *GhostContainer* pour cibler Microsoft Exchange.
*   **CVE-2019-0708 (BlueKeep) :** Exploitée pour obtenir des accès locaux et élever les privilèges sur les systèmes cibles.

**Recommandations :**
*   **Surveillance Active Directory :** Surveiller étroitement les requêtes de tickets Kerberos (flags suspects) et détecter toute tentative de réplication non autorisée (DCSync).
*   **Gestion des logs :** Auditer les journaux Windows, en particulier les événements liés aux services Bureau à distance (RDP) (IDs 132 et 148), pour détecter l'usage de canaux de communication anormaux associés à *rdp2tcp*.
*   **Durcissement des accès :** Imposer une authentification multifacteur (MFA) sur tous les accès VPN et appliquer les correctifs de sécurité critiques sur les serveurs Exchange et les systèmes exposés.
*   **Détection comportementale :** Utiliser des solutions EDR/NDR pour identifier les anomalies, telles que le chargement suspect d'assemblées .NET via PowerShell ou des connexions réseau vers des domaines de type `*.devtunnels.ms` initiées par des processus non autorisés.

---
[Source](https://securelist.com/tr/nighteagle-apt-ghostcontainer-and-tunneling/121323/){:target="_blank"}
