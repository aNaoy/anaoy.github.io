---
title: 'Ransomware gang abuses Microsoft Teams relays to hide malicious traffic'
date: 2026-06-16
permalink: /posts/2026/06/16/ransomware-gang-abuses-microsoft-teams-relays-to-hide-malicious-traffic/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement des relais Microsoft Teams par le ransomware DragonForce

Le groupe cybercriminel DragonForce a mis au point une nouvelle technique sophistiquée utilisant le malware **Backdoor.Turn** pour masquer son trafic de commande et contrôle (C2) au sein de l'infrastructure de relais TURN (*Traversal Using Relays around NAT*) de Microsoft Teams. Cette méthode permet aux attaquants de faire passer leurs communications malveillantes pour du trafic légitime, rendant la détection complexe.

**Points clés :**
*   **Technique "Ghost Calls" :** Exploitation des relais Teams pour créer des tunnels de communication furtifs via des serveurs de confiance.
*   **Tactique BYOVD (Bring Your Own Vulnerable Driver) :** Utilisation intensive de pilotes vulnérables pour obtenir des privilèges noyau et neutraliser les outils de sécurité (EDR/Antivirus).
*   **Infiltration :** L'intrusion initiale s'effectue via une exploitation de serveur SQL, suivie d'un chargement de DLL malveillantes (*sideloading*) pour établir la persistance.
*   **Capacités du malware :** Backdoor.Turn permet l'exécution de commandes, la recherche sur le réseau (LDAP/AD), le vol d'identifiants de navigateur et l'exfiltration de données avant le chiffrement final par le ransomware.

**Vulnérabilités exploitées (via des pilotes vulnérables) :**
*   **CVE-2023-52271 :** Pilote Topaz Antifraud (`wsftprm.sys`).
*   **CVE-2025-61155 :** Pilote Tower of Fantasy (`GameDriverx64.sys`).
*   **CVE-2025-1055 :** Pilote K7 Security (`K7RKScan.sys`).
*   *Note : Le pilote Huawei `HWAuidoOs2Ec.sys` et le pilote factice `ABYSSWORKER` ont également été utilisés.*

**Recommandations :**
*   **Surveillance réseau :** Analyser les connexions sortantes vers les infrastructures de communication tierces (Teams, Zoom) afin d'identifier des comportements anormaux ou des tunnels persistants inattendus.
*   **Gestion des pilotes :** Bloquer le chargement des pilotes vulnérables connus via des politiques de contrôle d'application (AppLocker, Windows Defender Application Control).
*   **Durcissement Windows :** Désactiver les politiques de sécurité laxistes, telles que l'autorisation de mots de passe vides (`LimitBlankPassword`), et renforcer la configuration des pare-feux locaux.
*   **Analyse des IoC :** Utiliser les indicateurs de compromission publiés par Symantec pour rechercher toute trace de Backdoor.Turn au sein du parc informatique.

---
[Source](https://www.bleepingcomputer.com/news/security/ransomware-gang-abuses-microsoft-teams-relays-to-hide-malicious-traffic/){:target="_blank"}
