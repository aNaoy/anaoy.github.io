---
title: 'Cursor Flaw Lets Malicious Cloned Repositories Trigger Windows Code Execution'
date: 2026-07-15
permalink: /posts/2026/07/15/cursor-flaw-lets-malicious-cloned-repositories-trigger-windows-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code dans l'IDE Cursor

L'IDE Cursor présente une faille de sécurité majeure sur Windows permettant l'exécution de code arbitraire sans interaction de l'utilisateur. Lorsqu'un projet est ouvert, Cursor recherche un exécutable nommé `git.exe` dans le dossier racine du répertoire de travail et l'exécute automatiquement. Un attaquant peut exploiter ce comportement en plaçant un fichier malveillant nommé `git.exe` à la racine d'un dépôt Git. Dès qu'une victime clone et ouvre ce dépôt dans Cursor, le binaire malveillant s'exécute avec les privilèges de l'utilisateur, accédant ainsi à ses clés SSH, jetons cloud et fichiers sources.

**Points clés :**
*   **Zero-click :** Aucune validation, boîte de dialogue ou approbation n'est requise.
*   **Persistance :** Le processus malveillant est relancé tant que le projet reste ouvert.
*   **Contexte :** Cette vulnérabilité découle d'une mauvaise gestion de l'ordre de recherche des exécutables sur Windows, où le répertoire courant est priorisé sur les chemins système sécurisés.
*   **Absence de correctif :** Bien que signalée en décembre 2025, aucune mise à jour corrective n'a été publiée par l'éditeur à ce jour.

**Vulnérabilités associées :**
*   Aucun identifiant CVE n'a été attribué par Cursor à cette faille.
*   Le problème s'inscrit dans une classe plus large d'attaques par "recherche de chemin non fiable" (similaire à **CVE-2020-26233**).

**Recommandations :**
*   **Sécurisation des environnements :** Utiliser des outils de contrôle d'application (AppLocker, Windows App Control) pour interdire l'exécution de binaires nommés `git.exe`, `npx.exe` ou `node.exe` situés dans des répertoires de projets.
*   **Isolation :** Ouvrir systématiquement les dépôts suspects ou provenant de sources non fiables dans une machine virtuelle dédiée ou via *Windows Sandbox*.
*   **Vigilance :** Inspecter le contenu des dossiers racines des dépôts clonés avant de les ouvrir avec un IDE, en recherchant la présence suspecte d'exécutables (`.exe`).
*   **Détection :** Privilégier les solutions EDR (Endpoint Detection and Response) capables de monitorer les comportements suspects des processus fils générés par les IDE.

---
[Source](https://thehackernews.com/2026/07/cursor-flaw-lets-malicious-cloned.html){:target="_blank"}
