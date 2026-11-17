---
title: 'New GitDoor and GraphDoor Backdoors Turn GitHub and SharePoint Into Covert C2 Channels'
date: 2026-11-17
permalink: /posts/2026/11/17/new-gitdoor-and-graphdoor-backdoors-turn-github-and-sharepoint-into-covert-c2-channels/
tags:
- veille-cyber
- hackernews
---
### Operation ShadowCloud : Des backdoors furtives exploitant le Cloud

L’opération « ShadowCloud » cible des secteurs gouvernementaux en Asie et en Afrique via deux nouvelles backdoors modulaires, **GitDoor** et **GraphDoor**. Ces menaces utilisent des services légitimes (GitHub, Microsoft SharePoint et Ably) pour leurs communications de commande et contrôle (C2), rendant leur trafic indiscernable d'une activité réseau normale.

**Points clés :**
*   **Vecteur initial :** Utilisation de l'outil de gestion à distance légitime *MeshCentral Agent*. La méthode d'infection initiale est inconnue, mais suggère une réutilisation d'accès existants sur des réseaux déjà compromis.
*   **Techniques de dissimulation :** Les payloads sont chiffrés et injectés directement en mémoire via des DLL malveillantes (sideloading). Le code utilise des techniques d'obfuscation avancées pour contrer l'analyse.
*   **Modularité :** Les deux backdoors permettent l'exécution de shellcodes, le téléchargement de plugins à la demande (keylogging, capture d'écran, extraction de mots de passe, vol de cookies) et la création de proxies SOCKS5 via Ably.
*   **Attribution :** Des similarités tactiques suggèrent une origine liée à des groupes d'espionnage basés en Chine (liens potentiels avec *Bronze Sandcastle*, *FamousSparrow* ou *BlackTech*).

**Vulnérabilités exploitées :**
L'attaque ne repose pas sur une CVE spécifique, mais sur l'abus de fonctionnalités légitimes :
*   **DLL Sideloading :** Utilisation d'exécutables signés (ex: `zoomit.exe`, `pythonw.exe`) pour charger des DLL malicieuses.
*   **Détournement d'API :** Utilisation abusive de Microsoft Graph API et des dépôts GitHub/SharePoint pour exfiltrer des données et recevoir des ordres.

**Recommandations :**
*   **Surveillance réseau :** Surveiller les flux de données sortants inhabituels vers les APIs Microsoft Graph, GitHub et le service de messagerie Ably, particulièrement s'ils proviennent de processus système ou d'outils d'administration.
*   **Contrôle des outils d'administration :** Restreindre l'installation et l'exécution de logiciels de contrôle distant comme *MeshCentral*. Implémenter une politique de moindre privilège pour empêcher l'exécution de code non autorisé.
*   **Détection d'exécution mémoire :** Déployer des solutions EDR capables de détecter l'injection de code (process hollowing/APC injection) et les comportements suspects liés au chargement de DLL non signées.
*   **Gestion des accès :** Auditer régulièrement les comptes utilisateurs locaux et les tâches planifiées pour identifier toute création anormale par des processus automatisés.

---
[Source](https://thehackernews.com/2026/11/new-gitdoor-and-graphdoor-backdoors.html){:target="_blank"}
