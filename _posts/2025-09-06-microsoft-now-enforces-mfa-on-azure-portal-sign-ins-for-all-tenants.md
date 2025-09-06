---
title: 'Microsoft now enforces MFA on Azure Portal sign-ins for all tenants'
date: 2025-09-06
permalink: /posts/2025/09/06/microsoft-now-enforces-mfa-on-azure-portal-sign-ins-for-all-tenants/
tags:
- veille-cyber
- bleepingcomp
---
**Renforcement de l'Authentification Multifacteur pour Azure**

Microsoft a achevé le déploiement de l'authentification multifacteur (MFA) pour toutes les connexions au portail Azure pour l'ensemble des locataires en mars 2025. Cette mesure vise à renforcer la protection des comptes et à prévenir les cyberattaques, notamment celles utilisant des identifiants compromis.

L'entreprise avait précédemment alerté les administrateurs globaux d'Entra à l'été 2024 pour qu'ils activent la MFA, sous peine de perdre l'accès aux portails d'administration à partir d'octobre 2024. Suite au succès de cette initiative pour le portail Azure, la MFA sera également imposée en octobre 2025 pour les outils tels qu'Azure CLI, PowerShell, les SDK et les API.

Une étude de Microsoft datant de deux ans a démontré que 99,99 % des comptes protégés par la MFA repoussent avec succès les tentatives de piratage, et que la MFA réduit le risque de compromission de compte de 98,56 %. L'objectif de Microsoft est d'atteindre 100 % d'utilisation de la MFA pour garantir une sécurité accrue.

**Points Clés :**

*   MFA désormais obligatoire pour toutes les connexions au portail Azure dans tous les locataires.
*   Déploiement achevé en mars 2025.
*   Extension de l'obligation MFA à Azure CLI, PowerShell, SDK et API à partir d'octobre 2025.
*   L'objectif est de minimiser les risques liés aux identifiants compromis.

**Vulnérabilités (non spécifiées dans l'article, mais implicitement liées à l'absence de MFA) :**

*   Utilisation d'identifiants volés ou devinés pour accéder aux ressources Azure.
*   Compromission de comptes d'administrateurs entraînant un accès non autorisé aux données et configurations.

**Recommandations :**

*   S'assurer que l'authentification multifacteur est activée pour tous les utilisateurs accédant aux portails et services Azure.
*   Se préparer à l'application obligatoire de la MFA pour les interfaces de ligne de commande et les SDK dès octobre 2025.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-now-enforces-mfa-on-azure-portal-sign-ins-for-all-tenants/){:target="_blank"}
