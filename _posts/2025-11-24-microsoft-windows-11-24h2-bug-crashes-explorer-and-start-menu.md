---
title: 'Microsoft: Windows 11 24H2 bug crashes Explorer and Start Menu'
date: 2025-11-24
permalink: /posts/2025/11/24/microsoft-windows-11-24h2-bug-crashes-explorer-and-start-menu/
tags:
- veille-cyber
- bleepingcomp
---
**Instabilité de l'Explorateur Windows 11 24H2 après les mises à jour cumulatives**

Microsoft a identifié un problème majeur affectant Windows 11 version 24H2, qui provoque des plantages du Gestionnaire de fichiers, du menu Démarrer et d'autres composants essentiels du système. Ce dysfonctionnement survient lors de la première connexion d'un utilisateur après l'application de mises à jour cumulatives publiées à partir de juillet 2025, ainsi que lors de toutes les connexions dans les environnements non persistants (comme les VDI). La cause réside dans un échec d'enregistrement des paquets de dépendance XAML (MicrosoftWindows.Client.CBS, Microsoft.UI.Xaml.CBS, MicrosoftWindows.Client.Core) après une mise à jour.

**Points clés :**

*   **Symptômes :** Plantages de l'Explorateur Windows (Explorer.exe), du Gestionnaire d'expérience du menu Démarrer (StartMenuExperienceHost), de l'Hôte de l'infrastructure shell (ShellHost.exe), erreurs critiques, absence de barre des tâches, ou application Paramètres qui ne se lance pas.
*   **Déclencheur :** Première connexion utilisateur après une mise à jour cumulative de juillet 2025 ou ultérieure pour Windows 11 24H2, ou toutes les connexions dans les environnements non persistants.
*   **Cause :** Problème de synchronisation dans l'enregistrement des paquets de dépendance XAML après l'installation d'une mise à jour.

**Vulnérabilités :**

Aucun identifiant CVE n'est explicitement mentionné pour ce problème spécifique dans l'article, mais il s'agit d'un défaut de fonctionnement causé par une mise à jour logicielle.

**Recommandations :**

*   **Solution temporaire :** L'exécution des commandes PowerShell suivantes pour enregistrer manuellement les paquets XAML manquants, suivie d'un redémarrage du système, peut restaurer la fonctionnalité :
    ```powershell
    Add-AppxPackage -Register -Path 'C:\Windows\SystemApps\MicrosoftWindows.Client.CBS_cw5n1h2txyewyppxmanifest.xml' -DisableDevelopmentMode
    Add-AppxPackage -Register -Path 'C:\Windows\SystemApps\Microsoft.UI.Xaml.CBS_8wekyb3d8bbweppxmanifest.xml' -DisableDevelopmentMode
    Add-AppxPackage -Register -Path 'C:\Windows\SystemApps\MicrosoftWindows.Client.Core_cw5n1h2txyewyppxmanifest.xml' -DisableDevelopmentMode
    ```
*   **Environnements non persistants :** Microsoft recommande d'exécuter un script de connexion (logon script) sur ces installations pour s'assurer que les paquets requis sont correctement provisionnés avant le chargement de l'environnement de bureau.
*   **Correction définitive :** Microsoft travaille sur une résolution permanente pour ce problème.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-11-24h2-bug-crashes-key-system-components/){:target="_blank"}
