---
title: 'SHub macOS infostealer variant spoofs Apple security updates'
date: 2026-05-19
permalink: /posts/2026/05/19/shub-macos-infostealer-variant-spoofs-apple-security-updates/
tags:
- veille-cyber
- bleepingcomp
---
### Menace macOS : Le voleur d'informations « SHub Reaper »

Une nouvelle variante du logiciel malveillant macOS, baptisée « Reaper », cible les utilisateurs via des sites de téléchargement frauduleux (WeChat, Miro). Ce programme détourne le protocole `applescript://` pour contourner les protections natives de macOS et exécuter des commandes malveillantes sous couvert d'une fausse mise à jour de sécurité Apple.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de l'éditeur de script système via des liens `applescript://`, évitant ainsi les restrictions de blocage du terminal imposées par Apple.
*   **Cibles :** Données de navigateurs, portefeuilles de cryptomonnaies (extensions et applications bureau), gestionnaires de mots de passe, fichiers sensibles (documents/bureau), comptes iCloud et sessions Telegram.
*   **Persistance :** Installation d'un agent de lancement (*LaunchAgent*) déguisé en mise à jour logicielle Google, s'exécutant chaque minute pour établir un accès distant.
*   **Évasion :** Le malware détecte les machines virtuelles, les VPN et les claviers russes (qu'il ignore volontairement). Il utilise la commande `xattr -cr` et la signature de code ad hoc pour neutraliser Gatekeeper.

**Vulnérabilités :**
Aucune CVE spécifique n'est exploitée ; le malware tire profit du comportement légitime de l'application *Script Editor* et de l'ingénierie sociale pour obtenir les privilèges utilisateur (demande de mot de passe macOS).

**Recommandations :**
*   **Surveillance réseau :** Analyser les communications sortantes suspectes initiées par l'application *Script Editor*.
*   **Audit système :** Vérifier la présence de nouveaux fichiers *LaunchAgents* ou de scripts suspects se faisant passer pour des services de mise à jour légitimes (Google, Apple).
*   **Vigilance :** Se méfier des sites web non officiels proposant des installeurs, même si l'interface semble familière.
*   **Sécurité des privilèges :** Être extrêmement prudent lors de la saisie de mots de passe système demandée par des fenêtres contextuelles inattendues.

---
[Source](https://www.bleepingcomputer.com/news/security/shub-macos-infostealer-variant-spoofs-apple-security-updates/){:target="_blank"}
