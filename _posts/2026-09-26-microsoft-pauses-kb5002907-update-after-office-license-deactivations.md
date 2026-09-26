---
title: 'Microsoft pauses KB5002907 update after Office license deactivations'
date: 2026-09-26
permalink: /posts/2026/09/26/microsoft-pauses-kb5002907-update-after-office-license-deactivations/
tags:
- veille-cyber
- bleepingcomp
---
### Suspension de la mise à jour Microsoft KB5002907 suite à des dysfonctionnements sur Office

Microsoft a suspendu le déploiement de la mise à jour **KB5002907**, initialement destinée à mettre à jour les installations Microsoft 365 obsolètes. Cette mise à jour provoque des effets indésirables majeurs sur les versions « perpétuelles » (licences à vie) d'Office 2016 et 2019.

**Points clés :**
*   **Problème constaté :** La mise à jour cible par erreur les licences Office 2016 et 2019, entraînant une désactivation logicielle (« Produit sans licence ») ou, dans des cas critiques, la désinstallation complète de la suite Office.
*   **Conflits d'architecture :** Des utilisateurs rapportent que le processus de réinstallation automatique échoue en présence d'un mélange d'architectures (ex: Office 32-bits avec Access Runtime 64-bits), laissant l'utilisateur sans aucune suite bureautique installée.
*   **Réaction de Microsoft :** L'éditeur a officiellement mis en pause la diffusion de KB5002907 via Windows Update pendant qu'une investigation est en cours.

**Vulnérabilités :**
*   Aucune CVE associée à ce problème, il s'agit d'un dysfonctionnement logiciel lié à la gestion des licences et des processus d'installation par Microsoft.

**Recommandations :**
*   **Si le produit est désactivé :** Tenter une réactivation en saisissant à nouveau la clé de produit originale ou en se connectant au compte Microsoft associé à la licence.
*   **Si Office a été supprimé :** Procéder à une réinstallation manuelle propre de la suite Office 2016 ou 2019 depuis le portail officiel Microsoft.
*   **Prévention :** Désactiver temporairement les mises à jour optionnelles si le parc informatique est composé majoritairement de versions Office non-abonnement, en attendant un correctif officiel de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-365-kb5002907-update-paused-after-office-license-deactivations/){:target="_blank"}
