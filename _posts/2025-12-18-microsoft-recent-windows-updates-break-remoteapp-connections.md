---
title: 'Microsoft: Recent Windows updates break RemoteApp connections'
date: 2025-12-18
permalink: /posts/2025/12/18/microsoft-recent-windows-updates-break-remoteapp-connections/
tags:
- veille-cyber
- bleepingcomp
---
**Problèmes de Connexion RemoteApp après Mises à Jour Windows**

Des mises à jour récentes de Windows, notamment KB5070311 de novembre 2025 et celles qui ont suivi, provoquent des échecs de connexion pour les utilisateurs de RemoteApp sur les versions Windows 11 24H2/25H2 et Windows Server 2025 dans des environnements Azure Virtual Desktop. Ce problème touche principalement les entreprises et n'affecte pas les sessions de bureau complètes ni les appareils personnels.

**Points Clés :**

*   **Impact:** Échec des connexions RemoteApp.
*   **Versions affectées:** Windows 11 24H2/25H2, Windows Server 2025.
*   **Mises à jour concernées:** KB5070311 (non-sécurisée) de novembre 2025 et ultérieures.
*   **Environnements touchés:** Azure Virtual Desktop, principalement dans un contexte d'entreprise.
*   **Non affectés:** Appareils personnels (éditions Home/Pro), sessions de bureau complètes.

**Vulnérabilités :**

Aucun identifiant CVE n'est spécifiquement mentionné pour ce problème.

**Recommandations :**

*   **Pour les organisations :**
    *   **Solution manuelle (avec droits administrateur) :**
        1.  Ouvrir l'invite de commandes en tant qu'administrateur.
        2.  Exécuter la commande : `reg add ""HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\WinLogon\ShellPrograms\RdpShell.exe" /v "ShouldStartRailRPC" /t REG_DWORD /d 1 /f`
        3.  Redémarrer l'appareil.
    *   **Utilisation du Known Issue Rollback (KIR) :**
        *   Pour les environnements gérés par l'IT, appliquer le rollback via une politique de groupe (Group Policy) spécifique à la version de Windows. Un fichier MSI pour l'installation et la configuration de cette politique est disponible.
        *   Redémarrer les appareils pour que la politique de groupe soit appliquée. Cette méthode désactivera temporairement la modification à l'origine du problème.
        *   Des guides pour déployer les politiques KIR sont disponibles sur le site de support de Microsoft.

Microsoft travaille sur une résolution permanente sans préciser de calendrier.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-recent-updates-break-azure-virtual-desktop-remoteapp-sessions/){:target="_blank"}
