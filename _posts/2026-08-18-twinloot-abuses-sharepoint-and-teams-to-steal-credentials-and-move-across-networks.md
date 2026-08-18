---
title: 'TWINLOOT Abuses SharePoint and Teams to Steal Credentials and Move Across Networks'
date: 2026-08-18
permalink: /posts/2026/08/18/twinloot-abuses-sharepoint-and-teams-to-steal-credentials-and-move-across-networks/
tags:
- veille-cyber
- hackernews
---
### Analyse du framework TWINLOOT : Exploitation des services Microsoft pour le C2

Le framework **TWINLOOT** est une menace Python modulaire et hautement furtive, conçue pour opérer intégralement via des services Microsoft légitimes afin d'échapper à la détection. Ce malware utilise le navigateur Edge de la victime en mode « headless » pour masquer ses communications réseau en tant que trafic légitime.

#### Points clés
*   **Infrastructure C2 hybride :** Utilise SharePoint Online (via Graph API) pour la réception des ordres, les serveurs TURN de Microsoft Teams pour les accès interactifs et un tunnel SOCKS5 pour le mouvement latéral.
*   **Vecteur d'infection :** Attaque par ingénierie sociale via Microsoft Teams, où l'attaquant usurpe le rôle du support informatique pour inciter la cible à exécuter un script PowerShell téléchargeant le payload.
*   **Méthodes de persistance avancées :** Utilise des techniques complexes incluant le détournement de scripts COM TypeLib, la manipulation du cache de tâches et l'utilisation de l'outil *Swarmer* pour créer des ruches de registre furtives via `NTUSER.MAN`.
*   **Vol d'identifiants :** Affiche de faux écrans de verrouillage Windows pour capturer les mots de passe des utilisateurs de manière transparente.

#### Vulnérabilités et vecteurs d'exploitation
*   **Abus de fonctionnalités légitimes (Living-off-the-land) :** Le malware n'exploite pas une vulnérabilité logicielle spécifique (CVE), mais détourne les API de communication légitimes (Microsoft Graph, WebRTC/TURN) et les mécanismes système (NTUSER.MAN).
*   **Technique "Ghost Calls" :** Exploitation du protocole WebRTC/TURN pour contourner les pare-feu et masquer les communications C2.

#### Recommandations de sécurité
*   **Sensibilisation :** Former les employés aux risques de l'ingénierie sociale sur les plateformes de communication (Teams, Slack), particulièrement les demandes d'exécution de scripts ou d'installation de logiciels inhabituels.
*   **Surveillance réseau :** Auditer les connexions sortantes vers les services cloud et surveiller l'usage inhabituel des protocoles WebRTC.
*   **Durcissement du système :**
    *   Limiter la capacité des utilisateurs à exécuter des scripts PowerShell non signés.
    *   Monitorer les modifications apportées au fichier `NTUSER.MAN` et les accès au registre via des APIs non standard.
    *   Restreindre l'utilisation des navigateurs en mode "headless" ou débogage via des politiques de groupe (GPO).
*   **Protection des identifiants :** Implémenter l'authentification multifacteur (MFA) sur tous les comptes pour atténuer l'impact du vol de mots de passe.

---
[Source](https://thehackernews.com/2026/08/twinloot-abuses-sharepoint-and-teams-to.html){:target="_blank"}
