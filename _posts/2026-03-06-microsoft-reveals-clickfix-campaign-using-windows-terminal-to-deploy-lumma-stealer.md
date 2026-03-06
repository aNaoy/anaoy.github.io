---
title: 'Microsoft Reveals ClickFix Campaign Using Windows Terminal to Deploy Lumma Stealer'
date: 2026-03-06
permalink: /posts/2026/03/06/microsoft-reveals-clickfix-campaign-using-windows-terminal-to-deploy-lumma-stealer/
tags:
- veille-cyber
- hackernews
---
### Campagne ClickFix : Exploitation du terminal Windows pour le déploiement de Lumma Stealer

Une nouvelle campagne d'ingénierie sociale de grande envergure, baptisée **ClickFix**, détourne les fonctionnalités légitimes du terminal Windows pour infiltrer des systèmes et déployer le malware **Lumma Stealer**. Contrairement aux méthodes habituelles utilisant la boîte de dialogue « Exécuter », les attaquants manipulent les utilisateurs pour qu'ils ouvrent directement le terminal via le raccourci `Windows + X` puis `I`, exploitant ainsi un environnement qui semble plus sécurisé et administratif.

#### Points clés
*   **Vecteur d'attaque :** Utilisation de fausses pages de CAPTCHA ou de messages de dépannage incitant l'utilisateur à copier-coller des commandes malveillantes (hexadécimales et compressées en XOR) dans le terminal Windows.
*   **Techniques de dissimulation :** Contournement des détections classiques ciblant la boîte de dialogue « Exécuter » et abus de « LOLBins » (*Living-off-the-Land Binaries*) comme `MSBuild.exe`.
*   **Persistance et exfiltration :** La chaîne d'attaque configure des exclusions dans Microsoft Defender, crée des tâches planifiées et injecte le malware dans les processus `chrome.exe` et `msedge.exe` via `QueueUserAPC()` pour dérober des identifiants et des données de navigation.
*   **Variante additionnelle :** Utilisation de scripts batch et VBScript, incluant des techniques de dissimulation de type *Etherhiding* (connexions à des endpoints RPC de blockchain).

#### Vulnérabilités exploitées
Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus de fonctionnalités légitimes du système d'exploitation et l'ingénierie sociale (absence de faille logicielle directe).

#### Recommandations
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les pages web demandant de copier-coller des commandes dans le terminal ou d'exécuter des scripts non vérifiés.
*   **Contrôle des privilèges :** Restreindre l'accès au terminal Windows et à PowerShell pour les utilisateurs standards lorsque cela n'est pas nécessaire.
*   **Surveillance et logs :** Surveiller les exécutions anormales de `wt.exe`, `powershell.exe` et `msbuild.exe`, en particulier celles invoquant des commandes encodées en base64 ou hexadécimales.
*   **Sécurité des endpoints :** Maintenir les solutions EDR/XDR à jour pour détecter les comportements d'injection de mémoire suspects (type `QueueUserAPC`) et les modifications non autorisées des exclusions de l'antivirus.

---
[Source](https://thehackernews.com/2026/03/microsoft-reveals-clickfix-campaign.html){:target="_blank"}
