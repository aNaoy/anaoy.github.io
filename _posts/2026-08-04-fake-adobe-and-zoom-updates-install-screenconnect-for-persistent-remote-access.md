---
title: 'Fake Adobe and Zoom Updates Install ScreenConnect for Persistent Remote Access'
date: 2026-08-04
permalink: /posts/2026/08/04/fake-adobe-and-zoom-updates-install-screenconnect-for-persistent-remote-access/
tags:
- veille-cyber
- hackernews
---
### Menaces persistantes : Abus des outils RMM et campagnes de vol d'informations

Deux campagnes malveillantes distinctes exploitent l'ingénierie sociale pour compromettre des systèmes, l'une utilisant des outils de gestion à distance légitimes et l'autre diffusant un logiciel espion sophistiqué via de faux cheats de jeux vidéo.

#### Campagne « SMOKE#SCREEN » : Abus des outils RMM
Cette campagne utilise des mises à jour factices (Adobe, Zoom) ou des documents professionnels pour déployer **ConnectWise ScreenConnect**, un outil de surveillance et de gestion à distance (RMM). L'objectif est d'obtenir un accès persistant sans éveiller les soupçons, en se fondant dans les outils informatiques autorisés.
*   **Vecteur d'attaque :** Phishing avec VBScript obfusqué, PowerShell, et utilisation de services de confiance (Dropbox, Cloudflare Tunnels) pour contourner les filtres de réputation.
*   **Points clés :** 
    *   Le malware détecte les environnements d'analyse (Wireshark, VirtualBox, Procmon) et s'interrompt pour éviter la détection.
    *   Des scripts automatisés désactivent les protections Windows (AMSI, SmartScreen, UAC) pour garantir l'installation.
*   **Recommandations :**
    *   Restreindre l'exécution de fichiers `.msi` non approuvés.
    *   Auditer rigoureusement l'utilisation des outils RMM au sein du parc informatique.
    *   Surveiller les activités suspectes des processus PowerShell et `cmd.exe`.
    *   Renforcer les paramètres UAC pour empêcher l'élévation de privilèges par les utilisateurs standards.

#### Campagne « Powercat » : Logiciel espion via faux cheats de jeux
Cette campagne cible les joueurs via de faux installeurs de "Xeno Executor" (utilisé pour tricher sur Roblox), diffusés sur des forums et Discord.
*   **Points clés :**
    *   Le malware (**Powercat**) est un logiciel espion Java multi-étapes capable de surveiller le clavier, l'écran et la webcam.
    *   Il exfiltre massivement des données : identifiants, cookies, portefeuilles de cryptomonnaies, données de messageries (Discord, Telegram, WhatsApp) et sessions de jeux.
    *   Le malware possède des capacités de contrôle à distance interactives via PowerShell.
*   **Cibles majeures :** Navigateurs, portefeuilles crypto (Exodus, Atomic, etc.), clients de jeux (Steam, Epic Games), messageries et VPN.

*Note : Aucune CVE spécifique n'est mentionnée pour ces campagnes, les attaquants abusant de fonctionnalités légitimes (Living-off-the-land) ou de techniques d'ingénierie sociale plutôt que de vulnérabilités logicielles identifiées.*

---
[Source](https://thehackernews.com/2026/08/fake-adobe-and-zoom-updates-install.html){:target="_blank"}
