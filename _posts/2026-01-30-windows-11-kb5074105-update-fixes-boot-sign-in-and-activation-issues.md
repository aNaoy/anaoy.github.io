---
title: 'Windows 11 KB5074105 update fixes boot, sign-in, and activation issues'
date: 2026-01-30
permalink: /posts/2026/01/30/windows-11-kb5074105-update-fixes-boot-sign-in-and-activation-issues/
tags:
- veille-cyber
- bleepingcomp
---
Mise à jour Windows 11 KB5074105 : Améliorations et Corrections

Microsoft a déployé la mise à jour cumulative optionnelle KB5074105 pour Windows 11, introduisant 32 modifications visant à résoudre des problèmes de démarrage, de connexion et d'activation. Cette mise à jour, disponible en fin de mois, permet aux administrateurs de tester les correctifs avant leur diffusion générale lors du Patch Tuesday du mois suivant. Il est important de noter que ces mises à jour mensuelles, non liées à la sécurité, se concentrent sur l'amélioration de la qualité et n'incluent pas de correctifs de sécurité.

**Points Clés :**

*   **Fonctionnalité Cross-Device Resume étendue :** Permet de reprendre des activités initiées sur un téléphone Android (lecture Spotify, travail sur Office, navigation web) directement sur le PC.
*   **Sécurité Renforcée pour Windows Hello :** La fonctionnalité Enhanced Sign-in Security (ESS) prend désormais en charge les capteurs d'empreintes digitales externes, étendant cette option de connexion sécurisée aux PC de bureau et autres appareils, y compris les Copilot+ PCs.
*   **Changements dans l'Identification des Mises à Jour :** À partir de janvier 2026, Windows Server 2025 aura ses propres identifiants (KB) et numéros de build, distincts de ceux de Windows 11 (versions 24H2 et 25H2), afin d'améliorer la clarté pour les administrateurs.
*   **Simplification des Titres de Mises à Jour :** Microsoft adopte des titres de mise à jour simplifiés pour une meilleure compréhension, en supprimant les éléments techniques superflus.

**Corrections Notables :**

*   **Résolution de blocages d'Explorateur.exe :** Un problème connu causant le blocage d'Explorer.exe lors de la première connexion, lorsque certaines applications étaient configurées au démarrage, a été corrigé.
*   **Stabilité au Démarrage :** Un bug entraînant l'arrêt de la réponse du système au démarrage lorsque le débogage du gestionnaire de démarrage Windows était activé a été corrigé.
*   **Correction des Échecs de Démarrage iSCSI :** Un bug provoquant des échecs de démarrage iSCSI avec l'erreur "Inaccessible Boot Device" a été résolu.
*   **Amélioration de la Migration des Licences Windows :** Un problème empêchant les migrations de licences Windows de réussir lors des mises à niveau, en raison de l'incapacité du PC à s'enregistrer auprès du serveur d'activation Windows, a été corrigé.
*   **Réponse du Terminal Windows :** Un problème où le PC pouvait cesser de répondre lors de la tentative d'exécution du Terminal Windows avec élévation de privilèges depuis un compte non-administrateur a été résolu.
*   **Erreurs Graphiques (KERNEL_SECURITY_CHECK_FAILURE) :** Un problème lié à dxgmms2.sys et provoquant une erreur système KERNEL_SECURITY_CHECK_FAILURE avec certaines configurations GPU a été corrigé.
*   **Blocage de Windows Sandbox :** Un problème pouvant entraîner le blocage de Windows Sandbox au démarrage avec l'erreur 0x800705b4 a été résolu.

**Vulnérabilités (CVE) :**

L'article ne mentionne pas de CVE spécifiques pour cette mise à jour optionnelle, car elle se concentre sur des améliorations de qualité et des corrections de bugs plutôt que sur des correctifs de sécurité.

**Recommandations :**

*   Installer la mise à jour KB5074105 via Windows Update en allant dans Paramètres > Windows Update > Rechercher les mises à jour, puis en cliquant sur "Télécharger et installer".
*   Il est également possible de télécharger et d'installer manuellement cette mise à jour depuis le Catalogue Microsoft Update.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5074105-update-fixes-boot-sign-in-and-activation-issues/){:target="_blank"}
