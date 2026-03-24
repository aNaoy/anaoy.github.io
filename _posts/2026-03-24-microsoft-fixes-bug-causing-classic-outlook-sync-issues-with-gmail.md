---
title: 'Microsoft fixes bug causing Classic Outlook sync issues with Gmail'
date: 2026-03-24
permalink: /posts/2026/03/24/microsoft-fixes-bug-causing-classic-outlook-sync-issues-with-gmail/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des problèmes de synchronisation dans Outlook Classic

Microsoft a déployé un correctif pour résoudre les erreurs de synchronisation (codes **0x800CCC0F** et **0x80070057**) affectant les comptes Gmail et Yahoo dans la version classique d'Outlook. Ces dysfonctionnements, apparus fin février 2026, empêchaient la connexion automatique aux comptes tiers.

**Points clés :**
*   Le correctif côté serveur est actif, mais une latence peut subsister jusqu'à l'expiration des jetons OAuth existants.
*   D'autres problèmes techniques persistent sur la plateforme, notamment des erreurs de connexion lors de la création de groupes Exchange, la disparition du pointeur de la souris dans les applications Microsoft 365, et des incompatibilités avec le complément "Microsoft Teams Meeting".

**Vulnérabilités :**
*   Aucune CVE associée à ce problème de synchronisation ; il s'agit d'un bug fonctionnel de gestion des jetons OAuth.

**Recommandations :**
*   **Attente automatique :** Le jeton OAuth expire généralement une heure après une modification de mot de passe, déclenchant automatiquement une demande de reconnexion.
*   **Action manuelle :** Si la synchronisation ne se rétablit pas, les utilisateurs peuvent forcer la réauthentification en supprimant les entrées d'identité correspondantes dans l'Éditeur du Registre Windows : 
    `Computer\HKEY_CURRENT_USER\Software\Microsoft\Office.0\Common\Identity\Identities`
*   **Support :** Pour les bugs persistants (comme le curseur invisible), il est conseillé de fournir des fichiers de diagnostic à Microsoft via un ticket de support administrateur.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bug-causing-outlook-sync-issues-for-gmail-users/){:target="_blank"}
