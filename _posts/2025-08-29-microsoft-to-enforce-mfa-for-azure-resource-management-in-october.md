---
title: 'Microsoft to enforce MFA for Azure resource management in October'
date: 2025-08-29
permalink: /posts/2025/08/29/microsoft-to-enforce-mfa-for-azure-resource-management-in-october/
tags:
- veille-cyber
- bleepingcomp
---
**Renforcement de l'authentification multifacteur (MFA) pour la gestion des ressources Azure**

À partir d'octobre 2025, Microsoft imposera l'authentification multifacteur (MFA) pour toutes les actions de gestion des ressources Azure. Cette mesure vise à protéger les clients Azure contre les tentatives d'accès non autorisées. L'application se fera progressivement pour les comptes se connectant via Azure CLI, PowerShell, les SDK et les API, incluant les scripts et l'automatisation utilisant des identités d'utilisateur.

**Points Clés :**

*   **Date d'entrée en vigueur :** Début progressif à partir du 1er octobre 2025.
*   **Portée :** Toutes les actions de création, mise à jour ou suppression de ressources Azure via les interfaces CLI, PowerShell, SDK et API, y compris l'automatisation utilisant des identités d'utilisateur. Concerne tous les locataires Azure dans le cloud public.
*   **Objectif :** Renforcer la sécurité et se prémunir contre les accès non autorisés, les comptes compromis et l'utilisation d'identifiants volés.
*   **Initiative de sécurité :** Fait partie de l'Initiative pour un Futur Sûr (SFI) de Microsoft.
*   **Délai de grâce :** Les administrateurs globaux peuvent reporter cette application jusqu'à juillet 2026.

**Vulnérabilités (non spécifiées dans l'article, mais le risque est l'accès non autorisé) :**

L'absence de MFA rend les comptes vulnérables aux compromissions par le biais d'identifiants volés ou devinés, permettant des actions non autorisées sur les ressources Azure.

**Recommandations :**

*   **Activer la MFA :** Assurez-vous que la MFA est activée pour tous les utilisateurs gérant des ressources Azure.
*   **Mettre à jour les outils :** Mettez à jour Azure CLI vers la version 2.76 ou ultérieure et Azure PowerShell vers la version 14.3 ou ultérieure pour éviter les problèmes de compatibilité.
*   **Surveillance :** Utilisez le rapport d'activité d'enregistrement des méthodes d'authentification ou le script PowerShell fourni pour suivre l'adoption de la MFA par les utilisateurs.
*   **Planification :** Si nécessaire, demandez un report de la date d'application avant la date limite.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-enforce-mfa-for-azure-resource-management-in-october/){:target="_blank"}
