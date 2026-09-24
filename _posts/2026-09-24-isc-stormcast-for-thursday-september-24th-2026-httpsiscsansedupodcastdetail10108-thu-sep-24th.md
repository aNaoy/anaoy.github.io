---
title: 'ISC Stormcast For Thursday, September 24th, 2026 https://isc.sans.edu/podcastdetail/10108, (Thu, Sep 24th)'
date: 2026-09-24
permalink: /posts/2026/09/24/isc-stormcast-for-thursday-september-24th-2026-httpsiscsansedupodcastdetail10108-thu-sep-24th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la menace : La montée des CAPTCHA trompeurs

L'article met en lumière une technique d'ingénierie sociale croissante où les attaquants détournent les interfaces de vérification humaine (CAPTCHA) pour compromettre la sécurité des terminaux.

**Points clés :**
*   **Mode opératoire :** Les utilisateurs sont incités à résoudre un faux CAPTCHA sur des sites web malveillants. Cette interaction déclenche le téléchargement d'un script malveillant (souvent PowerShell ou des fichiers binaires) sur l'ordinateur de la victime.
*   **Objectif :** L'exécution de ces scripts vise généralement à installer des logiciels malveillants, des infostealers ou à établir un accès persistant (backdoor) sur la machine cible.
*   **Complexité accrue :** Ces attaques exploitent la confiance des utilisateurs envers les outils de sécurité standards, rendant la détection initiale difficile pour les utilisateurs non avertis.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle (CVE) spécifique, mais plutôt d'une **vulnérabilité humaine** exploitant l'ingénierie sociale pour contourner les contrôles de sécurité (exécution de code arbitraire par l'utilisateur).

**Recommandations :**
*   **Sensibilisation :** Éduquer les utilisateurs sur le fait qu'un test CAPTCHA légitime ne demande jamais le téléchargement ou l'exécution d'un fichier sur l'ordinateur.
*   **Contrôles techniques :**
    *   Mettre en place des politiques d'exécution restreintes (AppLocker ou équivalent) pour empêcher l'exécution non autorisée de scripts PowerShell.
    *   Déployer des solutions de filtrage DNS et Web pour bloquer l'accès aux domaines malveillants connus servant de vecteurs de distribution.
    *   Utiliser des outils EDR (Endpoint Detection and Response) pour surveiller et alerter sur les processus suspects engendrés par des navigateurs web.

---
[Source](https://isc.sans.edu/diary/rss/33364){:target="_blank"}
