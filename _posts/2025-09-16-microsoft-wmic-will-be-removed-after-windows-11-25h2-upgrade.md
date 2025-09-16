---
title: 'Microsoft: WMIC will be removed after Windows 11 25H2 upgrade'
date: 2025-09-16
permalink: /posts/2025/09/16/microsoft-wmic-will-be-removed-after-windows-11-25h2-upgrade/
tags:
- veille-cyber
- bleepingcomp
---
**Abandon de WMIC : Vers des outils de gestion Windows plus modernes**

Microsoft retire progressivement l'outil en ligne de commande WMIC (Windows Management Instrumentation Command-line) de Windows 11 à partir de la version 25H2. WMIC, un outil hérité permettant d'interagir avec le système WMI via des commandes textuelles, est jugé obsolète au profit de solutions plus performantes et sécurisées.

**Points Clés :**

*   WMIC sera retiré de Windows 11 après la mise à niveau vers la version 25H2.
*   La technologie WMI sous-jacente reste inchangée.
*   Cette décision s'inscrit dans une démarche de modernisation des outils de gestion et de renforcement de la sécurité.

**Vulnérabilités :**

WMIC est identifié comme un "LOLBIN" (living-off-the-land binary), c'est-à-dire un exécutable légitime exploité par les acteurs malveillants. Les exemples d'utilisation malveillante incluent :

*   Suppression des copies de volume fantôme (Shadow Volume Copies) par les rançongiciels pour empêcher la récupération des données.
*   Interrogation de la liste des logiciels antivirus installés.
*   Désinstallation des logiciels antivirus.
*   Ajout d'exclusions à Microsoft Defender pour échapper à la détection.

Aucun CVE spécifique n'est mentionné pour ces utilisations, mais la nature du problème réside dans l'exploitation de l'outil par des tiers.

**Recommandations :**

*   **Migration vers PowerShell :** Les administrateurs IT sont fortement encouragés à migrer leurs scripts et tâches vers Windows PowerShell, solution recommandée par Microsoft pour interagir avec WMI.
*   **Exploration d'alternatives programmatiques :** D'autres alternatives incluent l'utilisation de l'API COM de WMI, des bibliothèques .NET, ou d'autres langages de script.
*   **Mise à jour de la documentation interne :** Il est essentiel d'adapter la documentation et les processus IT pour refléter ces changements.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-wmic-will-be-removed-after-windows-11-25h2-upgrade/){:target="_blank"}
