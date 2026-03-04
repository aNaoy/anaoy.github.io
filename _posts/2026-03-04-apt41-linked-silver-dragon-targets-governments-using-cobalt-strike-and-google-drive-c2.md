---
title: 'APT41-Linked Silver Dragon Targets Governments Using Cobalt Strike and Google Drive C2'
date: 2026-03-04
permalink: /posts/2026/03/04/apt41-linked-silver-dragon-targets-governments-using-cobalt-strike-and-google-drive-c2/
tags:
- veille-cyber
- hackernews
---
### Silver Dragon : La nouvelle menace ciblant les gouvernements

Un groupe de pirates informatiques sophistiqué, baptisé Silver Dragon et lié au groupe APT41 d'origine chinoise, a mené des cyberattaques contre des entités gouvernementales en Europe et en Asie du Sud-Est depuis mi-2024. L'objectif principal est l'espionnage, mais des activités financières pourraient également être en jeu.

**Méthodes d'attaque et infection :**

Silver Dragon utilise diverses techniques pour obtenir un accès initial et maintenir sa présence :

*   **Exploitation de serveurs publics :** Compromission de serveurs accessibles sur Internet.
*   **Phishing :** Envoi d'emails contenant des pièces jointes malveillantes (notamment des raccourcis Windows LNK) pour déclencher des scripts PowerShell.
*   **Vol de services Windows légitimes :** Hijacking de services pour camoufler les processus malveillants.
*   **Canaux de commande et contrôle (C2) par tunneling DNS :** Utilisation du DNS pour contourner la détection des communications avec les serveurs de contrôle.

**Outils et charges utiles :**

Le groupe déploie une panoplie d'outils et de logiciels malveillants :

*   **Cobalt Strike :** Utilisé pour maintenir la persistance sur les systèmes compromis.
*   **MonikerLoader :** Un chargeur basé sur .NET qui déchiffre et exécute des charges utiles de second étage en mémoire.
*   **BamboLoader :** Un chargeur de DLL, souvent injecté dans des processus légitimes comme "taskhost.exe".
*   **SilverScreen :** Un outil de surveillance d'écran capturant des captures d'écran périodiques, y compris la position du curseur.
*   **SSHcmd :** Un utilitaire SSH en ligne de commande pour l'exécution de commandes à distance et le transfert de fichiers.
*   **GearDoor :** Une porte dérobée .NET communiquant avec son infrastructure C2 via Google Drive.

**Utilisation de Google Drive pour le C2 :**

GearDoor exploite Google Drive de manière sophistiquée pour le contrôle des systèmes compromis :

*   Des fichiers avec des extensions spécifiques (*.png, *.pdf, *.cab, *.rar, *.7z) sont utilisés pour envoyer des informations sur le système, recevoir et exécuter des commandes, télécharger des fichiers, et même mettre à jour l'implant.
*   Les résultats des opérations sont renvoyés sous forme de fichiers avec différentes extensions (*.db, *.bak).

**Points clés et vulnérabilités :**

*   **Lien avec APT41 :** Des similitudes dans les scripts d'installation post-exploitation et les mécanismes de déchiffrement de BamboLoader renvoient à des activités précédemment attribuées à APT41.
*   **Techniques évolutives :** Le groupe adapte continuellement ses outils et techniques, démontrant une grande flexibilité et des ressources importantes.
*   **Vulnérabilités exploitées :** L'article mentionne des serveurs publics vulnérables et l'exploitation de DLL side-loading via des exécutables légitimes ("GameHook.exe"). Aucune vulnérabilité spécifique (CVE) n'est explicitement citée pour l'accès initial, mais l'usage de serveurs public facing et de techniques d'injection suggère l'exploitation de failles logicielles ou de mauvaises configurations.

**Recommandations (implicites) :**

Bien que l'article ne fournisse pas une liste formelle de recommandations, les informations présentées suggèrent les mesures suivantes :

*   **Renforcer la sécurité des serveurs publics :** Mettre à jour et patcher les systèmes exposés à Internet pour prévenir l'exploitation.
*   **Améliorer la détection du phishing :** Sensibiliser les utilisateurs aux risques et mettre en place des solutions de filtrage efficaces.
*   **Surveiller les activités suspectes :** Détecter les comportements anormaux liés à l'exécution de services, aux connexions réseau (tunneling DNS) et aux interactions avec des services cloud comme Google Drive.
*   **Sécuriser les environnements Google Workspace :** Mettre en place des politiques de sécurité renforcées pour Google Drive.
*   **Application de correctifs :** Maintenir tous les logiciels et systèmes d'exploitation à jour pour corriger les vulnérabilités connues.

---
[Source](https://thehackernews.com/2026/03/apt41-linked-silver-dragon-targets.html){:target="_blank"}
