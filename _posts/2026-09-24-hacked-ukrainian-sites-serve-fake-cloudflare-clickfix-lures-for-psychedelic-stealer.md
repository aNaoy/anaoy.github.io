---
title: 'Hacked Ukrainian Sites Serve Fake Cloudflare ClickFix Lures for Psychedelic Stealer'
date: 2026-09-24
permalink: /posts/2026/09/24/hacked-ukrainian-sites-serve-fake-cloudflare-clickfix-lures-for-psychedelic-stealer/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Campagne "ClickFix" et logiciel malveillant "Psychedelic Stealer"

Des attaquants exploitent des sites Web d'entreprises ukrainiennes pour injecter de fausses pages de vérification Cloudflare. Cette technique de « ClickFix » manipule les utilisateurs pour qu'ils copient et exécutent une commande PowerShell malveillante via l'outil « Exécuter » de Windows, permettant l'installation du logiciel espion **Psychedelic Stealer**. Parallèlement, une autre campagne utilise une approche similaire pour déployer **RemotePanel** (accès distant) et **BoundSiphon** (vol de données), ciblant les infrastructures critiques et les informations sensibles.

**Points clés :**
*   **Technique ClickFix :** Le leurre simule une vérification de sécurité et utilise une manipulation du presse-papier pour inciter l'utilisateur à exécuter un script MSI malveillant.
*   **Vol de données :** Psychedelic Stealer exfiltre les mots de passe des navigateurs, les jetons de session, les données de portefeuilles de cryptomonnaies et peut installer des extensions malveillantes.
*   **Modularité :** Le malware intègre des capacités d'exécution à distance (hVNC) et peut télécharger des charges utiles supplémentaires, témoignant d'une menace évolutive.
*   **Évasion :** Les attaquants utilisent des services légitimes (ex: BNB Smart Chain) pour résoudre leurs serveurs de commande et contrôle (C2), rendant la neutralisation difficile.
*   **Géolocalisation :** Les preuves techniques (langue, ciblage, exclusions de clavier russe) suggèrent une origine russophone visant principalement l'Ukraine.

**Vulnérabilités exploitées :**
*   **Contournement de l'UAC :** Utilisation de l'objet COM **CMSTPLUA** pour élever les privilèges sans intervention utilisateur.
*   **Détournement de processus :** Injection de code dans des processus Chromium légitimes pour contourner le chiffrement *App-Bound*.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à ne jamais copier-coller des commandes inconnues provenant d'Internet dans le menu « Exécuter » ou dans un terminal.
*   **Sécurisation des points de terminaison :** Bloquer l'exécution non autorisée de fichiers MSI via des politiques de groupe (GPO) et renforcer la surveillance des processus PowerShell.
*   **Filtrage Web :** Mettre en place une protection contre les scripts injectés et surveiller les domaines récemment enregistrés ou suspects associés aux campagnes « ClickFix ».
*   **Gestion des privilèges :** Restreindre les droits d'administration locale pour limiter l'impact en cas de compromission initiale.

---
[Source](https://thehackernews.com/2026/09/hacked-ukrainian-sites-serve-fake.html){:target="_blank"}
