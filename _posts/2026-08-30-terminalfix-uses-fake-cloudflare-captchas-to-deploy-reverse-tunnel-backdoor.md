---
title: 'TerminalFix Uses Fake Cloudflare CAPTCHAs to Deploy Reverse-Tunnel Backdoor'
date: 2026-08-30
permalink: /posts/2026/08/30/terminalfix-uses-fake-cloudflare-captchas-to-deploy-reverse-tunnel-backdoor/
tags:
- veille-cyber
- hackernews
---
### TerminalFix : Une menace par ingénierie sociale détournant Windows Terminal

**Points clés :**
*   **Méthode d'infection :** Utilisation de faux CAPTCHA Cloudflare sur des sites compromis pour inciter les utilisateurs à copier et exécuter un script PowerShell malveillant dans Windows Terminal ou PowerShell.
*   **Chaîne d'attaque :** Utilisation du "DLL sideloading" (chargement d'une DLL malveillante via un exécutable légitime) pour déployer une charge utile persistante.
*   **Extraction de données :** Utilisation de la stéganographie pour cacher les charges utiles dans des images PNG.
*   **Objectif :** Mise en place d'un tunnel inverse (via des WebSockets chiffrés) permettant aux attaquants un accès proxy complet au réseau interne de la victime, facilitant l'espionnage, l'énumération Active Directory et le déploiement futur de ransomwares.
*   **Persistance :** Mise en place de tâches planifiées et de clés de registre, couplée à une boucle de surveillance PowerShell capable d'exécuter des commandes arbitraires à distance.

**Vulnérabilités :**
*   Le vecteur principal repose sur l'ingénierie sociale (ClickFix) exploitant la confiance des utilisateurs envers les interfaces de sécurité.
*   **DLL Sideloading :** Exploitation de la gestion des bibliothèques dynamiques par Windows pour exécuter du code malveillant via des processus légitimes (ex: `dui70.dll` injecté dans `LockScreenContentServer.exe`).
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur des fonctionnalités légitimes du système d'exploitation détournées de leur usage.

**Recommandations :**
*   **Contrôle d'accès :** Restreindre l'exécution de PowerShell et de la boîte de dialogue "Exécuter" (Win+R) pour les utilisateurs standards via AppLocker, le contrôle d'application Windows ou les GPO.
*   **Surveillance :** Activer la journalisation des blocs de script PowerShell (*Script Block Logging*) pour détecter les commandes obfusquées.
*   **Détection :** Monitorer les comportements suspects liés au *DLL sideloading* et les connexions sortantes vers des infrastructures inconnues.
*   **Sensibilisation :** Former les employés aux campagnes de type "ClickFix" et à la méfiance vis-à-vis des invites de commande demandant une intervention manuelle via copier-coller.

---
[Source](https://thehackernews.com/2026/08/terminalfix-uses-fake-cloudflare.html){:target="_blank"}
