---
title: 'Microsoft Paint RCE Fix Now Available, but Windows Update Wont Deliver It'
date: 2026-11-06
permalink: /posts/2026/11/06/microsoft-paint-rce-fix-now-available-but-windows-update-wont-deliver-it/
tags:
- veille-cyber
- hackernews
---
### Correction de la faille RCE dans Microsoft Paint : mise à jour exclusive via le Microsoft Store

Une vulnérabilité critique a été identifiée dans l'application Microsoft Paint, permettant à un attaquant d'exécuter du code à distance (RCE). Contrairement aux mises à jour Windows classiques, le correctif est distribué exclusivement via le Microsoft Store.

**Points clés :**
*   **Vulnérabilité :** Il s'agit d'une faille de type « out-of-bounds read ».
*   **Gravité :** Évaluée comme « Important » par Microsoft, avec un score CVSS de 8,1.
*   **Vecteur d'attaque :** L'exploitation peut se faire via le réseau, sans interaction de l'utilisateur ni authentification, mais nécessite une connaissance approfondie du système cible.
*   **Distribution :** Le correctif ne passe pas par Windows Update. L'application doit être mise à jour via le Microsoft Store ou par des outils de gestion de parc informatique.
*   **Status :** Aucune exploitation active n'a été recensée à ce jour.

**Vulnérabilité identifiée :**
*   **CVE-2026-83844** : Correctif disponible à partir de la version **11.2609.401.0**.

**Recommandations :**
*   **Vérification des versions :** Étant donné que Paint est installé par utilisateur et qu'une copie « provisionnée » existe pour les nouveaux comptes, il est crucial de vérifier toutes les instances. Utilisez les commandes PowerShell suivantes (en mode administrateur) :
    *   `Get-AppxPackage -AllUsers -Name Microsoft.Paint | Select-Object Version, @{ n = 'Users'; e = { $_.PackageUserInformation.UserSecurityId.Username -join ', ' } }`
    *   `Get-AppxProvisionedPackage -Online | Where-Object DisplayName -eq 'Microsoft.Paint' | Select-Object Version`
*   **Mise à jour :** Assurez-vous que toutes les instances listées sont à jour vers la version **11.2609.401.0** ou ultérieure via le Microsoft Store.
*   **Suppression :** Si l'application n'est pas nécessaire, il est recommandé de la désinstaller pour toutes les instances (utilisateurs et provisionnement) pour réduire la surface d'attaque.

---
[Source](https://thehackernews.com/2026/11/microsoft-paint-rce-fix-now-available.html){:target="_blank"}
