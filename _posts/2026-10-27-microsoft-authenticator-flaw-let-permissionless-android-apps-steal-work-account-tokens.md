---
title: 'Microsoft Authenticator Flaw Let Permissionless Android Apps Steal Work Account Tokens'
date: 2026-10-27
permalink: /posts/2026/10/27/microsoft-authenticator-flaw-let-permissionless-android-apps-steal-work-account-tokens/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité majeure dans Microsoft Authenticator pour Android : vol de jetons d'accès

Une faille critique a été identifiée dans l'application Microsoft Authenticator sur Android, permettant à des applications malveillantes, même dépourvues de permissions spécifiques, d'usurper l'identité d'applications Microsoft légitimes (comme Teams) pour dérober des jetons d'authentification.

**Points clés :**
*   **Mécanisme de l'attaque :** L'application malveillante exploite l'activité `AccountChooserActivity` d'Authenticator. En fournissant des paramètres contrefaits, l'attaquant force le "broker" (Authenticator) à croire qu'il s'agit d'une application Microsoft légitime déjà présente sur l'appareil.
*   **Échec de sécurité :** Bien qu'un mécanisme de vérification de signature existe, il échoue car il valide la signature de l'application légitime installée sur l'appareil plutôt que celle de l'application appelante.
*   **Impact :** L'obtention de ces jetons permet à un attaquant d'accéder aux ressources professionnelles de l'utilisateur, incluant les e-mails, les fichiers et le calendrier, avec les mêmes privilèges que le compte compromis.
*   **État de la menace :** Microsoft indique qu'aucune exploitation active n'a été constatée à ce jour, bien que la vulnérabilité soit jugée importante avec un score CVSS de 8,6.

**Vulnérabilité :**
*   **CVE-2026-80097 :** Problème d'usurpation d'identité dans la gestion des jetons via le broker d'Authenticator.

**Recommandations :**
*   **Mise à jour immédiate :** Mettre à jour l'application Microsoft Authenticator vers la version **6.2606.4246** ou ultérieure.
*   **Gestion de flotte :** Les organisations utilisant des solutions MDM (Mobile Device Management) doivent appliquer une politique imposant cette version minimale sur l'ensemble des appareils Android gérés.

---
[Source](https://thehackernews.com/2026/10/microsoft-authenticator-flaw-let.html){:target="_blank"}
