---
title: 'Windows 11 cumulative updates KB5124008 & KB5122880 released'
date: 2026-09-08
permalink: /posts/2026/09/08/windows-11-cumulative-updates-kb5124008-kb5122880-released/
tags:
- veille-cyber
- bleepingcomp
---
### Mises à jour cumulatives de septembre 2026 : Windows 11 KB5124008 et KB5122880

Microsoft a déployé les mises à jour cumulatives obligatoires **KB5124008** (pour Windows 11 25H2/24H2) et **KB5122880** (pour la version 23H2). Elles intègrent le *Patch Tuesday* de septembre 2026, corrigeant plus de 1 000 vulnérabilités identifiées ces derniers mois.

**Points clés :**
*   **Protection des administrateurs :** Introduction de l'« Administrator Protection » (désactivé par défaut), permettant d'utiliser des privilèges *just-in-time* pour limiter les attaques par élévation de privilèges.
*   **Isolation des processus :** Mise en place de l'isolation pour les « Microsoft Execution Containers » (MXC) afin de restreindre l'accès aux ressources système (fichiers, réseau, UI) pour les processus légers.
*   **Agentic Processes :** Support en préversion du marquage des processus d'agents (IA) pour sécuriser leur authentification via le Web Account Manager (WAM).
*   **Améliorations fonctionnelles :** Personnalisation étendue de la barre des tâches (position, taille), refonte du menu Démarrer et optimisation de Windows Search (plus de contrôle sur les suggestions Web).

**Vulnérabilités :**
*   L'article mentionne la correction de 1 000 vulnérabilités, mais ne liste aucune CVE spécifique.

**Recommandations :**
*   **Installation immédiate :** Ces mises à jour étant obligatoires et critiques pour la sécurité, il est fortement conseillé de les installer via *Windows Update* ou via le *Microsoft Update Catalog*.
*   **Activation des nouvelles protections :** Pour les administrateurs système, il est recommandé d'évaluer et d'activer la fonctionnalité « Administrator protection » via Microsoft Intune ou les stratégies de groupe (GPO) pour renforcer la sécurité des privilèges élevés.
*   **Gestion des agents :** Suivre l'évolution de la nouvelle plateforme de marquage des processus d'agents si votre infrastructure utilise des agents IA.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-cumulative-updates-kb5124008-and-kb5122880-released/){:target="_blank"}
