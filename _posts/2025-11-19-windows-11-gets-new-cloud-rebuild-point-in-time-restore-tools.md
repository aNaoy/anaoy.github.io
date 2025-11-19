---
title: 'Windows 11 gets new Cloud Rebuild, Point-in-Time Restore tools'
date: 2025-11-19
permalink: /posts/2025/11/19/windows-11-gets-new-cloud-rebuild-point-in-time-restore-tools/
tags:
- veille-cyber
- bleepingcomp
---
**Améliorations de la Récupération de Windows 11 : Restauration et Reconstruction Simplifiées**

Microsoft introduit deux nouvelles fonctionnalités majeures pour Windows 11 afin de réduire les temps d'arrêt et de simplifier la reprise après des échecs système ou des mises à jour problématiques, dans le cadre de son Initiative de Résilience Windows. Ces outils visent à permettre aux organisations de restaurer rapidement les appareils devenus non fonctionnels.

**Fonctionnalités Clés :**

*   **Point-in-Time Restore (PITR) :** Permet de revenir à un état antérieur sain du système en quelques minutes. Contrairement à la restauration système classique, PITR crée des instantanés complets du système à différents moments, restaurant également les fichiers et applications locaux. Cette fonctionnalité sera bientôt disponible en avant-première dans une build Insider de Windows 11.

*   **Cloud Rebuild :** Outil permettant de déclencher à distance une réinstallation complète de Windows 11 depuis le cloud pour les appareils présentant des problèmes persistants ou devenus inopérants. Les administrateurs pourront sélectionner la version de Windows et la langue via le portail Intune. Le processus utilise Autopilot pour un provisionnement sans intervention, assure l'enregistrement MDM et la conformité des politiques, et utilise OneDrive et Windows Backup for Organizations pour la restauration des données et paramètres utilisateur. L'objectif est de réduire le temps de reprise de plusieurs heures ou jours à une fraction de ce temps.

Ces deux fonctionnalités seront intégrées à Microsoft Intune au cours du premier semestre 2026, offrant aux administrateurs la possibilité de déclencher des actions de récupération à distance, de coordonner la remédiation à l'échelle de l'entreprise et de gérer les fonctionnalités de l'environnement de récupération Windows (WinRE) directement depuis Intune.

Microsoft teste également une version améliorée de Quick Machine Recovery (QMR), un outil qui aide les administrateurs à résoudre les échecs de démarrage de Windows sans accès physique. En cas d'échec de démarrage, QMR se lance automatiquement, envoie des informations de crash à Microsoft qui peut alors appliquer des correctifs à distance (suppression de pilotes problématiques, désinstallation de mises à jour, modification de configurations). La nouvelle version optimise ce processus en effectuant une seule analyse pour détecter et résoudre les problèmes, évitant ainsi des boucles de recherche répétitives.

**Points Clés :**

*   Introduction de Cloud Rebuild et Point-in-Time Restore (PITR) pour Windows 11.
*   Objectif : réduire les temps d'arrêt et faciliter la reprise après incidents.
*   PITR permet de restaurer le système, les paramètres, les fichiers et applications à un état antérieur.
*   Cloud Rebuild permet une réinstallation complète de Windows 11 depuis le cloud via Intune.
*   Intégration future dans Microsoft Intune au premier semestre 2026.
*   Amélioration de Quick Machine Recovery (QMR) pour une résolution plus rapide des échecs de démarrage.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans l'article. L'accent est mis sur les nouvelles fonctionnalités de *récupération* et de *résilience* plutôt que sur la correction de failles de sécurité existantes.

**Recommandations :**

*   Les administrateurs systèmes devraient se familiariser avec ces nouvelles fonctionnalités pour optimiser les stratégies de reprise après incident.
*   Exploiter l'intégration avec Microsoft Intune pour une gestion centralisée et à distance des processus de récupération.
*   Tester les nouvelles builds Insider pour évaluer les capacités de PITR.
*   Suivre le déploiement complet de Cloud Rebuild et PITR prévu pour le premier semestre 2026.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-gets-new-cloud-rebuild-point-in-time-restore-tools/){:target="_blank"}
