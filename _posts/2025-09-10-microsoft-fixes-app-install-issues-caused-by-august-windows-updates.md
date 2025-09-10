---
title: 'Microsoft fixes app install issues caused by August Windows updates'
date: 2025-09-10
permalink: /posts/2025/09/10/microsoft-fixes-app-install-issues-caused-by-august-windows-updates/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour Windows : Résolution des problèmes d'installation d'applications et d'invites UAC**

Une faille de sécurité corrigée par les mises à jour d'août 2025 provoquait des problèmes d'installation d'applications et des invites de contrôle de compte d'utilisateur (UAC) inattendues pour les utilisateurs non administrateurs sur toutes les versions de Windows.

**Points clés :**

*   Les mises à jour de sécurité d'août 2025 ont corrigé une vulnérabilité d'escalade de privilèges du programme d'installation Windows.
*   La correction a entraîné des problèmes où les utilisateurs non administrateurs étaient confrontés à des invites UAC excessives lors de l'installation d'applications ou de l'utilisation de certaines fonctionnalités du programme d'installation Windows.
*   Une nouvelle mise à jour en septembre 2025 réduit la portée des invites UAC pour les réparations MSI et offre aux administrateurs informatiques la possibilité de désactiver ces invites pour des applications spécifiques.

**Vulnérabilité corrigée :**

*   **CVE-2025-50173** : Vulnérabilité d'escalade de privilèges du programme d'installation Windows.

**Plateformes affectées :**

*   **Client :** Windows 11 (versions 24H2, 23H2, 22H2), Windows 10 (versions 22H2, 21H2, 1809), Windows 10 Enterprise LTSC 2019, Windows 10 Enterprise LTSC 2016, Windows 10 (version 1607), Windows 10 Enterprise 2015 LTSB.
*   **Serveur :** Windows Server 2025, Windows Server 2022, Windows Server (version 1809), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows Server 2012.

**Recommandations :**

*   Installer les mises à jour de sécurité de septembre 2025 ou les versions ultérieures de Windows.
*   Pour les administrateurs informatiques, utiliser les clés de registre `SecureRepairPolicy` et `SecureRepairWhitelist` sous `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Installer` pour créer une liste d'autorisation d'applications pour lesquelles les invites UAC seront désactivées.
*   Les invites UAC ne seront requises lors des opérations de réparation MSI qu'en cas d'action personnalisée élevée dans le fichier MSI cible.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-app-install-issues-caused-by-august-windows-updates/){:target="_blank"}
