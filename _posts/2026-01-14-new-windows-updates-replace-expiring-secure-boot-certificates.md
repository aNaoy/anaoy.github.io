---
title: 'New Windows updates replace expiring Secure Boot certificates'
date: 2026-01-14
permalink: /posts/2026/01/14/new-windows-updates-replace-expiring-secure-boot-certificates/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour des certificats de démarrage sécurisé sous Windows**

Microsoft déploie activement de nouveaux certificats de démarrage sécurisé (Secure Boot) pour les systèmes Windows 11 24H2 et 25H2 éligibles. Cette démarche vise à remplacer les certificats actuels dont l'expiration est prévue en juin 2026.

Le démarrage sécurisé est une fonctionnalité essentielle des systèmes UEFI qui garantit que seul un logiciel de démarrage approuvé peut s'exécuter au lancement de l'ordinateur, empêchant ainsi l'exécution de logiciels malveillants tels que les rootkits. L'expiration des certificats actuels pourrait compromettre cette protection, rendant les appareils incapables de démarrer de manière sécurisée et de recevoir des mises à jour de sécurité pour les composants de pré-amorçage.

**Points Clés :**

*   **Expiration des certificats :** Les certificats de démarrage sécurisé actuels expireront en juin 2026.
*   **Impact :** Sans certificats mis à jour, les appareils pourraient ne plus bénéficier des protections du démarrage sécurisé et ne pas recevoir de futures mises à jour de sécurité.
*   **Déploiement automatique :** Microsoft met à jour automatiquement les appareils considérés comme ayant une "haute confiance" via Windows Update.
*   **Options de déploiement pour les administrateurs :** Les organisations peuvent également déployer les nouveaux certificats via des clés de registre, le système de configuration Windows (WinCS) et les stratégies de groupe.

**Recommandations :**

*   **Administrateurs IT :** Il est conseillé d'inventorier les parcs d'appareils, de vérifier le statut du démarrage sécurisé et d'appliquer les mises à jour du firmware des fabricants avant d'installer les nouveaux certificats de Microsoft.
*   **Utilisateurs :** S'assurer que les mises à jour de Windows sont appliquées pour bénéficier du déploiement automatique.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-rolls-out-new-secure-boot-certificates-for-windows-devices/){:target="_blank"}
