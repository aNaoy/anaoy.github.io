---
title: 'Windows 11 gets new Cloud Rebuild, Point-in-Time Restore tools'
date: 2025-11-19
permalink: /posts/2025/11/19/windows-11-gets-new-cloud-rebuild-point-in-time-restore-tools/
tags:
- veille-cyber
- bleepingcomp
---
**Améliorations de la récupération sous Windows 11**

Microsoft introduit deux nouvelles fonctionnalités de récupération pour Windows 11 : Cloud Rebuild et Point-in-Time Restore (PITR), dans le cadre de l'initiative Windows Resiliency. Ces outils visent à réduire les temps d'arrêt et à simplifier la restauration après des défaillances système ou des mises à jour problématiques.

**Points clés :**

*   **Point-in-Time Restore (PITR) :** Permet de revenir à un instantané antérieur du système, incluant le système d'exploitation, les paramètres, les fichiers système, ainsi que les fichiers et applications locaux. Cette fonctionnalité améliore la fonction "Restauration du système" existante en capturant des instantanés complets. Elle sera bientôt disponible en préversion dans une build Insider.
*   **Cloud Rebuild :** Un outil permettant de déclencher à distance une réinstallation complète de Windows 11 depuis le cloud via le portail Intune. Les administrateurs peuvent sélectionner la version et la langue de Windows souhaitées. Le processus utilise Autopilot pour un provisionnement sans intervention, assure l'inscription MDM et la conformité des stratégies. La restauration des données utilisateur et des paramètres est facilitée par OneDrive et Windows Backup for Organizations.
*   **Intégration Intune :** Les deux fonctionnalités seront intégrées à Microsoft Intune au cours du premier semestre 2026, permettant aux administrateurs de déclencher des actions de récupération à distance, de coordonner les remédiations à l'échelle de l'entreprise et de contrôler l'environnement de récupération Windows (WinRE).
*   **Améliorations de Quick Machine Recovery (QMR) :** Microsoft teste également une version améliorée de QMR, un outil qui aide les administrateurs à résoudre les échecs de démarrage de Windows sans accès physique. La nouvelle version effectue un scan unique pour détecter et résoudre les problèmes, au lieu de boucles de recherche répétées.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans cet article concernant ces nouvelles fonctionnalités.

**Recommandations :**

*   Les administrateurs devraient se familiariser avec ces nouvelles fonctionnalités de récupération lors de leur déploiement, notamment leur intégration avec Microsoft Intune.
*   Il est conseillé de tester la fonctionnalité PITR lors de sa disponibilité en préversion pour évaluer son efficacité dans les environnements spécifiques.
*   L'adoption de Cloud Rebuild et de ses capacités de provisionnement zéro-touch via Autopilot pourrait considérablement réduire les temps d'arrêt lors de problèmes système majeurs.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-gets-new-cloud-rebuild-point-in-time-restore-tools/){:target="_blank"}
