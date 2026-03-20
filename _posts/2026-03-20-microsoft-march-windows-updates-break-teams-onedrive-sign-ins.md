---
title: 'Microsoft: March Windows updates break Teams, OneDrive sign-ins'
date: 2026-03-20
permalink: /posts/2026/03/20/microsoft-march-windows-updates-break-teams-onedrive-sign-ins/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnements de connexion après la mise à jour Windows de mars

La mise à jour cumulative **KB5079473**, déployée lors du « Patch Tuesday » de mars, provoque des erreurs de connexion sur Windows 11 pour les comptes Microsoft personnels.

**Points clés :**
* **Applications impactées :** Microsoft Teams, OneDrive, Edge, la suite Office (Word, Excel) et Microsoft 365 Copilot.
* **Symptômes :** Les utilisateurs reçoivent un message d'erreur indiquant une absence de connexion Internet, même si l'appareil est correctement relié au réseau.
* **Périmètre :** Seuls les comptes Microsoft personnels sont affectés. Les entreprises utilisant *Entra ID* (anciennement Azure Active Directory) ne sont pas concernées.
* **Autres correctifs récents :** Microsoft a publié des mises à jour correctives (OOB) pour résoudre des problèmes de visibilité Bluetooth et des vulnérabilités critiques dans le service RRAS (*Routing and Remote Access Service*).

**Vulnérabilités mentionnées :**
* Plusieurs failles de sécurité non spécifiées dans l'outil de gestion RRAS (traitées via des mises à jour hors bande).

**Recommandations :**
* **Contournement temporaire :** Redémarrer l'appareil tout en maintenant une connexion Internet active. Il est impératif que l'ordinateur soit connecté au réseau lors du redémarrage pour réinitialiser l'état de connectivité.
* **Cas spécifique Samsung :** Pour les utilisateurs de PC portables Samsung rencontrant des problèmes d'accès au disque C:, Microsoft recommande de vérifier la version de l'application *Samsung Galaxy Connect* (ou *Samsung Continuity Service*), responsable de certains conflits logiciels.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/kb5079473-march-windows-11-update-breaks-microsoft-account-sign-ins/){:target="_blank"}
