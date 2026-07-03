---
title: 'PamStealer Uses Fake Maccy Sites and PAM Checks to Steal Mac Login Passwords'
date: 2026-07-03
permalink: /posts/2026/07/03/pamstealer-uses-fake-maccy-sites-and-pam-checks-to-steal-mac-login-passwords/
tags:
- veille-cyber
- hackernews
---
### PamStealer : Une nouvelle menace ciblant les utilisateurs de macOS

Le logiciel malveillant **PamStealer** cible les utilisateurs de macOS en se faisant passer pour l'application légitime *Maccy*. Il utilise une chaîne d'infection sophistiquée basée sur des scripts AppleScript et une charge utile en Rust pour dérober des données sensibles, notamment les mots de passe système.

**Points clés :**
*   **Vecteur d'infection :** Distribution via des sites web frauduleux (ex: `maccyapp[.]com`) imitant le site officiel.
*   **Technique de contournement :** Utilisation d'un fichier `.scpt` qui contourne les protections Gatekeeper en exploitant l'interaction manuelle de l'utilisateur (raccourci clavier) pour exécuter le code malveillant.
*   **Vérification de l'environnement :** Le malware n'exécute sa charge utile que sur les systèmes Apple Silicon et évite les environnements analysés ou localisés en Europe de l'Est.
*   **Validation via PAM :** Le logiciel utilise l'interface *Pluggable Authentication Modules* (PAM) pour vérifier la validité du mot de passe saisi par l'utilisateur avant de l'exfiltrer.
*   **Persistence et leurre :** Après avoir volé les données (clés iCloud, données de navigation, portefeuilles crypto), il affiche un faux message d'erreur système pour inciter la victime à supprimer le fichier malveillant, masquant ainsi son activité.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle spécifique avec un CVE, mais de l'exploitation de **mécanismes natifs macOS** (AppleScript, exécution via Script Editor) et de l'ingénierie sociale pour contourner les protections par défaut (Gatekeeper).

**Recommandations :**
*   **Sources officielles uniquement :** Téléchargez des logiciels uniquement depuis le site web officiel du développeur ou le Mac App Store. Pour *Maccy*, l'unique adresse officielle est `maccy.app`.
*   **Vigilance sur l'exécution de scripts :** Ne jamais exécuter des fichiers `.scpt` ou des commandes suggérées par des sites web inconnus via l'éditeur de script.
*   **Analyse du comportement :** Méfiez-vous des applications qui demandent des privilèges élevés (accès complet au disque) et qui affichent des messages d'erreur "application endommagée" immédiatement après une installation.
*   **Mise à jour :** Maintenez macOS à jour pour bénéficier des dernières protections contre les logiciels malveillants, bien que cette menace utilise des fonctions légitimes du système pour opérer.

---
[Source](https://thehackernews.com/2026/07/pamstealer-uses-fake-maccy-sites-and.html){:target="_blank"}
