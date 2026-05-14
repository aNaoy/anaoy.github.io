---
title: 'Iranian hackers targeted major South Korean electronics maker'
date: 2026-05-14
permalink: /posts/2026/05/14/iranian-hackers-targeted-major-south-korean-electronics-maker/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'espionnage du groupe MuddyWater

Le groupe de cyberespionnage MuddyWater (Seedworm), lié à l'Iran, a mené une vaste campagne visant neuf organisations internationales, incluant un fabricant d'électronique majeur en Corée du Sud, des agences gouvernementales, un aéroport et des établissements d'enseignement. Les attaquants se concentrent principalement sur le vol de propriété intellectuelle et l'espionnage industriel.

**Points clés**
*   **Technique d'intrusion :** Utilisation intensive du *DLL sideloading* en détournant des logiciels légitimes signés (utilitaires Fortemedia et SentinelOne).
*   **Outils malveillants :** Déploiement de *ChromElevator* pour le vol de données dans les navigateurs et utilisation de loaders Node.js pour piloter des scripts PowerShell.
*   **Exfiltration :** Utilisation du service de partage de fichiers public `sendit.sh` pour masquer le trafic sortant et le faire paraître légitime.
*   **Persistance :** Modifications du registre Windows et relances répétées des binaires compromis pour maintenir l'accès.

**Vulnérabilités exploitées**
L'attaque ne repose pas sur une vulnérabilité logicielle spécifique (CVE), mais sur l'abus de fonctionnalités système et de logiciels de confiance :
*   **DLL Sideloading :** Exploitation de la méthode de recherche de bibliothèques dynamiques par Windows.
*   **Abus de protocoles et outils :** Exploitation de PowerShell, WMI, et des outils Kerberos pour le mouvement latéral et le vol d'identifiants (via le dump des ruches SAM/SECURITY/SYSTEM).

**Recommandations**
*   **Surveillance des processus :** Auditer les logs pour détecter l'exécution de binaires légitimes signés chargeant des DLL suspectes à partir de répertoires non standard.
*   **Contrôle des privilèges :** Restreindre l'accès aux ruches du registre système et surveiller l'utilisation suspecte de PowerShell par des comptes non autorisés.
*   **Filtrage réseau :** Bloquer ou surveiller étroitement les flux vers les services de partage de fichiers publics non approuvés pour prévenir l'exfiltration de données.
*   **Détection des comportements :** Mettre en place des alertes sur des activités anormales telles que l'énumération antivirus via WMI ou la création de tunnels SOCKS5.

---
[Source](https://www.bleepingcomputer.com/news/security/iranian-hackers-targeted-major-south-korean-electronics-maker/){:target="_blank"}
