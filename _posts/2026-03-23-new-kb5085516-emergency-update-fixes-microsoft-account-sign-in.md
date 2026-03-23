---
title: 'New KB5085516 emergency update fixes Microsoft account sign-in'
date: 2026-03-23
permalink: /posts/2026/03/23/new-kb5085516-emergency-update-fixes-microsoft-account-sign-in/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif d'urgence Microsoft : résolution des erreurs de connexion aux comptes

Une mise à jour cumulative récente (KB5079473) a provoqué un dysfonctionnement majeur empêchant la connexion aux comptes Microsoft sur Windows 11. Ce bug affecte des applications telles que Teams, OneDrive, Edge, Microsoft 365 Copilot et la suite Office, affichant à tort une erreur de connectivité Internet. Seuls les comptes personnels sont concernés, les entreprises utilisant Entra ID (Azure AD) ne sont pas impactées.

**Points clés :**
* **Origine :** Le problème est apparu suite au déploiement du Patch Tuesday de mars 2026.
* **Symptômes :** Message d'erreur indiquant une absence de connexion Internet lors de l'authentification, malgré une connexion active.
* **Portée :** Utilisateurs de Windows 11 (versions 25H2 et 24H2) utilisant un compte Microsoft personnel.

**Vulnérabilités :**
* Aucun CVE spécifique lié à ce bug fonctionnel. (Note : l'article mentionne par ailleurs des correctifs récents pour une faille RCE dans le service RRAS).

**Recommandations :**
* **Installation du correctif :** Installer la mise à jour optionnelle **KB5085516** via Windows Update ou le Microsoft Update Catalog.
* **Solution temporaire :** En cas d'impossibilité de mise à jour immédiate, redémarrer l'appareil pour tenter de réinitialiser les services réseau.
* **Maintenance générale :** S'assurer que les systèmes sont à jour, Microsoft ayant également corrigé récemment des problèmes liés au Bluetooth et des vulnérabilités de sécurité critiques dans le service RRAS.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/new-kb5085516-emergency-update-fixes-microsoft-account-sign-in/){:target="_blank"}
