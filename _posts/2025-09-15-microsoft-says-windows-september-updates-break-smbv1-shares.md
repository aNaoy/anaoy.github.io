---
title: 'Microsoft says Windows September updates break SMBv1 shares'
date: 2025-09-15
permalink: /posts/2025/09/15/microsoft-says-windows-september-updates-break-smbv1-shares/
tags:
- veille-cyber
- bleepingcomp
---
### Mises à jour Windows de Septembre Interrompent l'Accès aux Partages SMBv1

Les correctifs de sécurité Windows de septembre 2025 entraînent des problèmes de connexion aux partages utilisant le protocole SMBv1 sur NetBIOS sur TCP/IP (NetBT). Ce défaut affecte diverses versions de Windows clients (Windows 11 24H2/23H2/22H2, Windows 10 22H2/21H2) et serveurs (Windows Server 2025, Windows Server 2022).

Le dysfonctionnement survient si le client ou le serveur SMB a appliqué les mises à jour de septembre 2025 ou ultérieures. Microsoft travaille sur une solution définitive, mais propose une mesure temporaire : autoriser le trafic sur le port TCP 445 pour forcer l'utilisation de TCP au lieu de NetBT pour les connexions SMB.

SMBv1, obsolète depuis 2007 et non installé par défaut sur les versions récentes de Windows, présente des failles de sécurité significatives. Il est dépourvu des améliorations de sécurité des versions plus récentes, comme les contrôles d'intégrité pré-authentification et la protection contre les attaques par dégradation. Des exploits tels qu'EternalBlue et EternalRomance, basés sur ces vulnérabilités, ont été exploités par des malwares majeurs comme WannaCry et NotPetya.

**Points Clés :**

*   Les mises à jour de sécurité Windows de septembre 2025 perturbent la connectivité aux partages SMBv1.
*   L'impact concerne un large éventail de versions de Windows client et serveur.
*   Le problème est lié à l'utilisation de NetBIOS sur TCP/IP pour les connexions SMBv1.
*   SMBv1 est un protocole ancien et intrinsèquement moins sécurisé, qui a été progressivement abandonné par Microsoft.

**Vulnérabilités :**

Bien qu'aucun numéro CVE spécifique ne soit mentionné pour ce dysfonctionnement actuel, le protocole SMBv1 lui-même est considéré comme vulnérable en raison de son manque de fonctionnalités de sécurité modernes. Historiquement, des vulnérabilités dans SMBv1 ont été exploitées par des malwares tels que :

*   EternalBlue
*   EternalRomance

Ces exploits ont été utilisés dans des attaques majeures comme WannaCry et NotPetya.

**Recommandations :**

*   **Priorité :** Désactiver complètement SMBv1 sur tous les systèmes. Microsoft recommande cette mesure depuis des années en raison des risques de sécurité.
*   **Solution Temporaire :** En attendant une correction, autoriser le trafic sur le port TCP 445 pour les connexions SMB, forçant ainsi l'utilisation du protocole TCP plus sûr.
*   **Mise à Jour :** Installer les futurs correctifs de sécurité de Microsoft dès leur disponibilité pour résoudre le problème de manière permanente.
*   **Migration :** Migrer les systèmes et les partages vers des versions plus récentes et sécurisées du protocole SMB (SMBv2 ou SMBv3).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-says-windows-september-updates-break-smbv1-shares/){:target="_blank"}
