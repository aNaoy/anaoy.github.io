---
title: 'APT41-Linked Silver Dragon Targets Governments Using Cobalt Strike and Google Drive C2'
date: 2026-03-04
permalink: /posts/2026/03/04/apt41-linked-silver-dragon-targets-governments-using-cobalt-strike-and-google-drive-c2/
tags:
- veille-cyber
- hackernews
---
**"Dragon d'Argent" : La Menace APT41 Ciblent les Gouvernements**

Un groupe de menace persistante avancée (APT) nommé "Dragon d'Argent" est actif depuis au moins mi-2024, ciblant des entités gouvernementales en Europe et en Asie du Sud-Est. Ce groupe est considéré comme faisant partie de l'écosystème APT41, un groupe de pirates informatiques chinois connu pour ses activités d'espionnage et potentiellement pour des motivations financières.

**Techniques et Outils Employés :**

*   **Accès initial :** Exploitation de serveurs publics exposés sur Internet et campagnes d'hameçonnage (phishing) avec des pièces jointes malveillantes.
*   **Maintien de la persistance :** Piratage de services Windows légitimes pour masquer les processus malveillants. Utilisation de Cobalt Strike pour maintenir la présence sur les systèmes compromis.
*   **Communication de commande et contrôle (C2) :** Techniques de tunneling DNS pour contourner la détection. Utilisation de Google Drive pour la communication C2, avec des extensions de fichiers spécifiques (*.png, *.pdf, *.cab, *.rar, *.7z) dictant les actions à entreprendre et la manière de rapporter les résultats.
*   **Chaînes d'infection identifiées :**
    *   **Pirâtage d'AppDomain et DLL de service :** Ces méthodes, livrées via des archives compressées, sont utilisées dans des scénarios post-exploitation suite au compromis de serveurs vulnérables. Elles impliquent des scripts batch, des chargeurs comme MonikerLoader et BamboLoader, et l'injection de shellcode dans des processus légitimes (ex: "taskhost.exe").
    *   **Hameçonnage par raccourcis Windows (LNK) :** Principalement ciblant l'Ouzbékistan, ces fichiers LNK lancent du code PowerShell pour télécharger et exécuter des charges utiles. Cela inclut un document d'apparence légitime comme couverture, une DLL malveillante (BamboLoader) exploitant une vulnérabilité de "DLL side-loading" dans "GameHook.exe", et une charge utile Cobalt Strike chiffrée ("simhei.dat").
*   **Outils post-exploitation :**
    *   **SilverScreen :** Outil de surveillance d'écran pour capturer des captures d'écran périodiques.
    *   **SSHcmd :** Utilitaire de ligne de commande SSH pour l'exécution à distance de commandes et le transfert de fichiers.
    *   **GearDoor :** Porte dérobée (backdoor) communiquant via Google Drive, présentant des similitudes avec MonikerLoader.

**Points Clés :**

*   Le groupe "Dragon d'Argent" est associé à APT41, un acteur majeur dans le paysage des menaces cybernétiques chinoises.
*   Les attaques ciblent spécifiquement des entités gouvernementales.
*   Une forte utilisation de Cobalt Strike et de techniques d'évasion avancées, notamment via Google Drive pour le C2.
*   Les méthodes d'infection et les outils démontrent une évolution constante et une adaptabilité du groupe.

**Vulnérabilités (non spécifiées avec CVE dans l'article) :**

L'article mentionne l'exploitation de :
*   Serveurs publics exposés sur Internet.
*   Vulnérabilités dans des exécutables légitimes permettant le "DLL side-loading" (ex: "GameHook.exe").

**Recommandations :**

Bien que l'article se concentre sur les tactiques du groupe, les recommandations implicites pour contrer de telles menaces incluent :
*   **Sécurisation des périmètres :** Renforcer la sécurité des serveurs publics exposés sur Internet et patcher les vulnérabilités connues.
*   **Sensibilisation au phishing :** Former les utilisateurs à reconnaître et signaler les e-mails de phishing et les pièces jointes suspectes.
*   **Surveillance et détection :** Mettre en place des solutions de surveillance réseau etEndpoint Detection and Response (EDR) robustes pour détecter les comportements anormaux, y compris l'utilisation de Cobalt Strike et les communications C2 inhabituelles.
*   **Gestion des services et des processus :** Surveiller les modifications apportées aux services Windows légitimes et les processus suspects.
*   **Politiques de sécurité strictes :** Appliquer des politiques de sécurité rigoureuses concernant l'utilisation des applications et le téléchargement de fichiers.
*   **Analyse des journaux :** Examiner attentivement les journaux d'événements pour identifier des signes d'intrusion ou de mouvements latéraux.

---
[Source](https://thehackernews.com/2026/03/apt41-linked-silver-dragon-targets.html){:target="_blank"}
