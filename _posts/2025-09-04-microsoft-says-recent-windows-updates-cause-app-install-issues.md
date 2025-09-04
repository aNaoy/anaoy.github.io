---
title: 'Microsoft says recent Windows updates cause app install issues'
date: 2025-09-04
permalink: /posts/2025/09/04/microsoft-says-recent-windows-updates-cause-app-install-issues/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour Windows d'août 2025 : Impact sur l'installation d'applications et la gestion des privilèges**

Les mises à jour de sécurité Windows d'août 2025 introduisent des problèmes inattendus pour les utilisateurs non administrateurs, entraînant des erreurs lors de l'installation et de la réparation d'applications. Ce comportement est lié à une mesure de sécurité renforcée visant à corriger une vulnérabilité d'escalade de privilèges.

**Points clés :**

*   Les mises à jour d'août 2025 (notamment KB5063878) imposent une vérification plus stricte des privilèges administrateur pour les opérations d'installation et de réparation via Windows Installer (MSI).
*   Les utilisateurs standards peuvent rencontrer des blocages pour des actions telles que la réparation de programmes, l'installation d'applications configurées pour un utilisateur spécifique, ou l'exécution de certaines tâches liées à Active Setup.
*   Certains logiciels, comme des versions spécifiques d'Autodesk (AutoCAD, Civil 3D, Inventor CAM), peuvent également être affectés.
*   Les plateformes clientes et serveurs de Windows, des versions récentes aux versions plus anciennes supportées, sont concernées.

**Vulnérabilité corrigée :**

*   **CVE-2025-50173** : Vulnérabilité d'escalade de privilèges dans Windows Installer permettant à des attaquants authentifiés d'obtenir des privilèges SYSTEM.

**Recommandations :**

*   **Solution temporaire pour les utilisateurs :** Exécuter les applications nécessitant des opérations MSI en tant qu'administrateur.
*   **Solution pour les environnements gérés :** Les administrateurs informatiques peuvent solliciter le support technique de Microsoft pour déployer des correctifs spécifiques via Known Issue Rollback (KIR) sur les versions concernées de Windows 11 et Windows Server 2025/2022, et Windows 10.
*   **Correction à venir :** Microsoft travaille sur une mise à jour pour permettre aux administrateurs d'autoriser spécifiquement certaines applications à effectuer des opérations MSI sans demander de privilèges UAC.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-says-recent-windows-updates-cause-app-install-issues-due-to-unexpected-admin-UAC-prompts/){:target="_blank"}
