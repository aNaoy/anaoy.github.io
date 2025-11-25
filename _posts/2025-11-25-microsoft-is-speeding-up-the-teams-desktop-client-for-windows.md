---
title: 'Microsoft is speeding up the Teams desktop client for Windows'
date: 2025-11-25
permalink: /posts/2025/11/25/microsoft-is-speeding-up-the-teams-desktop-client-for-windows/
tags:
- veille-cyber
- bleepingcomp
---
**Amélioration des performances de Microsoft Teams pour Windows**

Microsoft introduira début 2026 un nouveau gestionnaire d'appels pour l'application de bureau Teams sous Windows. Ce changement vise à réduire les temps de lancement et à améliorer les performances des appels.

Un nouveau processus, `ms-teams_modulehost.exe`, sera utilisé parallèlement au processus principal `ms-teams.exe` pour gérer les fonctionnalités d'appel. Cette modification architecturale est conçue pour optimiser l'utilisation des ressources et l'expérience des réunions sans altérer le flux de travail des utilisateurs ni nécessiter de formation supplémentaire.

**Points Clés:**

*   **Date de déploiement :** Début janvier 2026, achevé fin janvier 2026.
*   **Fonctionnalité :** Introduction de `ms-teams_modulehost.exe` pour gérer les appels de manière séparée du processus principal de l'application.
*   **Objectif :** Améliorer les temps de démarrage et les performances des appels dans Teams pour Windows.
*   **Impact utilisateur :** Aucun changement dans le workflow ou l'apparence des fonctionnalités d'appel pour les utilisateurs finaux.

**Vulnérabilités:**

Aucune vulnérabilité spécifique avec identifiant CVE n'est mentionnée dans cet article. L'article traite d'une amélioration de performance et de sécurité opérationnelle, et non de la correction d'une faille de sécurité existante.

**Recommandations:**

*   **Administrateurs IT :**
    *   Ajouter `ms-teams_modulehost.exe` à la liste blanche des logiciels de sécurité et des systèmes de protection des terminaux pour éviter les fausses détections et les problèmes d'appel.
    *   Informer le personnel de support technique de l'existence de ce nouveau processus pour faciliter le dépannage et prévenir toute confusion.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-boost-teams-performance-with-new-call-handler/){:target="_blank"}
