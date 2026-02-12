---
title: 'Windows 11 Notepad flaw let files execute silently via Markdown links'
date: 2026-02-12
permalink: /posts/2026/02/12/windows-11-notepad-flaw-let-files-execute-silently-via-markdown-links/
tags:
- veille-cyber
- bleepingcomp
---
## L'Éditeur Notepad de Windows 11 : Une Faille de Sécurité Corrigée

Une faille critique dans l'application Bloc-notes de Windows 11, permettant l'exécution silencieuse de code à distance, a été corrigée par Microsoft. Cette vulnérabilité exploitait le support du format Markdown, récemment introduit dans l'application.

En manipulant des liens spécifiquement conçus dans des fichiers Markdown, un attaquant pouvait inciter un utilisateur à cliquer, déclenchant ainsi l'exécution de programmes locaux ou distants sans aucune alerte de sécurité Windows. L'exploit tirait parti de protocoles non vérifiés et de liens directs vers des exécutables ou des installateurs d'applications, s'exécutant avec les privilèges de l'utilisateur.

**Points Clés :**

*   **Exécution de Code à Distance :** La faille permettait à des attaquants d'exécuter du code sur la machine de la victime.
*   **Support Markdown Exploité :** L'ajout de la prise en charge du format Markdown dans le Bloc-notes de Windows 11 a ouvert la porte à cette vulnérabilité.
*   **Absence d'Alertes :** Les programmes s'exécutaient sans déclencher les avertissements de sécurité habituels de Windows.
*   **Impact :** Potentiel d'exécution de fichiers malveillants à partir de partages réseau distants.

**Vulnérabilité :**

*   **CVE :** CVE-2026-20841
*   **Description :** Neutralisation inappropriée d'éléments spéciaux utilisés dans une commande ("injection de commande") dans l'application Bloc-notes de Windows, permettant à un attaquant non autorisé d'exécuter du code sur un réseau.

**Recommandations :**

*   **Mise à Jour Immédiate :** Les utilisateurs de Windows 11 doivent s'assurer que leur application Bloc-notes est mise à jour via le Microsoft Store. La correction a été déployée lors des mises à jour de sécurité de février 2026.
*   **Prudence avec les Liens :** Bien que corrigée, la vulnérabilité illustre l'importance de la prudence lors du clic sur des liens, même dans des applications de confiance. Les versions corrigées de Bloc-notes afficheront désormais un avertissement pour les liens ne utilisant pas les protocoles `http://` ou `https://`.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-notepad-flaw-let-files-execute-silently-via-markdown-links/){:target="_blank"}
