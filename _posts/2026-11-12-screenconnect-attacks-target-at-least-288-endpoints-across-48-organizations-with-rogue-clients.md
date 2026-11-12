---
title: 'ScreenConnect Attacks Target at Least 288 Endpoints Across 48 Organizations With Rogue Clients'
date: 2026-11-12
permalink: /posts/2026/11/12/screenconnect-attacks-target-at-least-288-endpoints-across-48-organizations-with-rogue-clients/
tags:
- veille-cyber
- hackernews
---
### Campagne de compromission via des extensions ScreenConnect

Une campagne malveillante exploitant des instances ScreenConnect a été identifiée, touchant au moins 288 points de terminaison dans 48 organisations. Contrairement à une faille logicielle directe, les attaquants détournent des extensions tierces ou accèdent aux panneaux de contrôle via des identifiants compromis pour déployer le kit malveillant **SCKit**.

#### Points clés
*   **Mode opératoire :** Les attaquants utilisent la fonction "Run Command" de ScreenConnect pour installer des clients distants non autorisés, assurant une persistance indépendante du panneau initial.
*   **Propagation latérale :** Le logiciel malveillant tente de rebondir sur les postes des techniciens qui se connectent aux machines infectées, visant à voler des jetons de session pour étendre l'accès à d'autres panneaux ScreenConnect.
*   **Automatisation :** Certains scripts utilisés semblent avoir été générés par des outils d'IA et le processus est automatisé pour cibler massivement les environnements des fournisseurs de services managés (MSP).
*   **Vulnérabilité :** Aucune CVE n'est associée à cet incident ; il s'agit d'une exploitation d'extensions tierces et de compromissions de comptes (identifiants volés ou sessions détournées).

#### Extensions désactivées par précaution par ConnectWise
*   Labtech Plus
*   RMM Plus / RMM+
*   RMM Plus Password Link / RMM+ Password Link

#### Recommandations de sécurité
*   **Audit immédiat :** Vérifier l'historique des commandes "Run Command" sur vos instances ScreenConnect, même en l'absence d'alertes.
*   **Surveillance active :** Porter une attention particulière aux nouveaux comptes administrateurs, aux changements de permissions inattendus, aux installations d'extensions non approuvées et aux comportements anormaux des outils de support (Toolbox).
*   **Contrôle d'accès :** Renforcer la sécurité des sessions, s'assurer que l'authentification multifacteur (MFA) est strictement appliquée et auditer régulièrement les accès aux APIs.
*   **Détection :** Rechercher la présence d'artefacts suspects, notamment les scripts nommés `sckit-run.bat`, `sckit-decoder.ps1`, `Panel-Lateral.ps1` ou la tâche planifiée nommée `TrapWatch`.
*   **Confinement :** En cas de doute, isoler les machines suspectes et révoquer les sessions actives des techniciens sur les instances compromises.

---
[Source](https://thehackernews.com/2026/11/screenconnect-attacks-target-at-least.html){:target="_blank"}
