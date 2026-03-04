---
title: 'APT41-Linked Silver Dragon Targets Governments Using Cobalt Strike and Google Drive C2'
date: 2026-03-04
permalink: /posts/2026/03/04/apt41-linked-silver-dragon-targets-governments-using-cobalt-strike-and-google-drive-c2/
tags:
- veille-cyber
- hackernews
---
## Silver Dragon : La Nouvelle Menace Ciblant les Gouvernements

Un groupe de cybercriminels persistants avancé (APT), surnommé Silver Dragon, est actif depuis mi-2024, ciblant des organisations en Europe et en Asie du Sud-Est. Ce groupe, présumé lié à l'APT41 d'origine chinoise, concentre ses attaques sur les entités gouvernementales.

### Points Clés :

*   **Cible Principale :** Entités gouvernementales en Europe et en Asie du Sud-Est.
*   **Affiliation :** Suspecté d'opérer sous l'égide de l'APT41, un groupe connu pour des activités d'espionnage et potentiellement lucratives.
*   **Techniques d'Infiltration :** Exploitation de serveurs accessibles publiquement, emails d'hameçonnage avec pièces jointes malveillantes.
*   **Maintien de Persistance :** Détournement de services Windows légitimes pour masquer les processus malveillants.
*   **Commandement et Contrôle (C2) :** Utilisation de DNS tunneling et de Google Drive pour contourner la détection.
*   **Outils Utilisés :** Cobalt Strike, MonikerLoader, BamboLoader, SilverScreen, SSHcmd, GearDoor.

### Vulnérabilités et Vecteurs d'Attaque :

Les méthodes d'infection initiales identifiées incluent :

*   **Détournement d'AppDomain :** Via des archives compressées contenant des scripts batch, menant à l'exécution de MonikerLoader, un chargeur .NET qui exécute des charges utiles secondaires en mémoire.
*   **DLL de Service :** Également via des archives compressées, un script batch déploie BamboLoader, une DLL obfuscée enregistrée comme service Windows. Celle-ci décompresse et injecte du shellcode dans des processus légitimes comme "taskhost.exe".
*   **Campagne d'Hameçonnage :** Principalement dirigée vers l'Ouzbékistan, utilisant des raccourcis Windows (LNK) malveillants. Ces fichiers lancent du code PowerShell pour télécharger et exécuter des charges utiles, incluant un document factice, un exécutable vulnérable ("GameHook.exe") permettant le chargement latéral de DLL, une DLL malveillante ("graphics-hook-filter64.dll") et une charge utile chiffrée de Cobalt Strike ("simhei.dat").

Les outils de post-exploitation déployés incluent :

*   **SilverScreen :** Outil de surveillance d'écran capturant l'activité utilisateur.
*   **SSHcmd :** Utilititaire SSH pour l'exécution de commandes à distance et le transfert de fichiers.
*   **GearDoor :** Une porte dérobée communiquant via Google Drive.

L'utilisation de Google Drive comme canal C2 est notable. GearDoor utilise différentes extensions de fichiers (*.png, *.pdf, *.cab, *.rar, *.7z) pour envoyer des informations système, recevoir des commandes, exécuter des tâches, transférer des fichiers et charger des plugins ou des mises à jour.

Les liens avec APT41 proviennent de similarités dans les scripts d'installation post-exploitation et du mécanisme de déchiffrement de BamboLoader observé dans des activités APT liées à la Chine. Le groupe fait preuve d'une adaptabilité et d'une sophistication notables en utilisant des exploits variés, des chargeurs personnalisés et des communications C2 basées sur des fichiers.

### Recommandations :

Bien que l'article ne détaille pas de recommandations spécifiques de manière exhaustive, les techniques employées suggèrent les mesures suivantes :

*   **Sécurisation des Serveurs Publiquement Exposés :** Appliquer des correctifs et des mesures de sécurité pour les serveurs accessibles depuis Internet.
*   **Sensibilisation à l'Hameçonnage :** Éduquer les utilisateurs à reconnaître et signaler les emails suspects et les pièces jointes malveillantes.
*   **Surveillance du Trafic Réseau :** Mettre en place des systèmes de détection d'intrusion et surveiller les communications DNS et l'utilisation de services Cloud comme Google Drive pour des activités suspectes.
*   **Gestion des Vulnérabilités :** Maintenir un inventaire des actifs et appliquer régulièrement les mises à jour de sécurité pour les logiciels et systèmes d'exploitation afin de corriger les vulnérabilités exploitées (ex: DLL side-loading).
*   **Analyse des Processus et Services :** Surveiller l'apparition de processus suspects ou le détournement de services Windows légitimes.
*   **Analyse des Charges Utiles :** Utiliser des solutions de sécurité capables de détecter et d'analyser les malwares .NET, les shellcodes et les artefacts d'exécution en mémoire.

Il n'y a pas de CVE spécifiques mentionnés dans cet article.

---
[Source](https://thehackernews.com/2026/03/apt41-linked-silver-dragon-targets.html){:target="_blank"}
