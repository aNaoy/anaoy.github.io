---
title: 'New cPanel Flaw Lets a Hosting Account With Mail Privileges Run Code as Root'
date: 2026-09-09
permalink: /posts/2026/09/09/new-cpanel-flaw-lets-a-hosting-account-with-mail-privileges-run-code-as-root/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans cPanel : Escalade de privilèges vers Root

Une faille de sécurité majeure affectant toutes les versions supportées de cPanel et WHM permet à un utilisateur disposant de privilèges liés à la messagerie d'exécuter du code arbitraire avec des droits **root**.

**Points clés :**
*   **Vecteur d'attaque :** La vulnérabilité réside dans la fonctionnalité `EmailTrack`. Bien que décrite comme une injection SQL, elle permet à un attaquant de créer des fichiers sur le serveur, menant à une exécution de code à distance.
*   **Impact :** Une prise de contrôle totale du serveur (via WHM), permettant à l'attaquant d'accéder aux données, d'installer des malwares ou de compromettre d'autres comptes hébergés.
*   **Vulnérabilité :** CVE-2026-67401.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquez les correctifs fournis par cPanel en mettant à jour votre système vers les versions suivantes (ou supérieures) :
    *   11.110.0.143
    *   11.134.0.55
    *   11.136.0.39
    *   11.138.0.4
    *   WP Squared : 11.138.1.9
*   **Procédure :** Via l'interface WHM sous *Home / cPanel / Upgrade to Latest Version* ou en ligne de commande avec la commande : `/usr/local/cpanel/scripts/upcp --force` en tant que root.
*   **Vigilance :** Surveillez les journaux d'accès pour détecter toute activité suspecte, car aucun mécanisme n'est actuellement documenté pour vérifier si un serveur a déjà été compromis avant l'application du correctif.

---
[Source](https://thehackernews.com/2026/09/new-cpanel-flaw-lets-hosting-account.html){:target="_blank"}
