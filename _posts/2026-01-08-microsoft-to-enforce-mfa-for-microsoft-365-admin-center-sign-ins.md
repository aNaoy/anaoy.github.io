---
title: 'Microsoft to enforce MFA for Microsoft 365 admin center sign-ins'
date: 2026-01-08
permalink: /posts/2026/01/08/microsoft-to-enforce-mfa-for-microsoft-365-admin-center-sign-ins/
tags:
- veille-cyber
- bleepingcomp
---
**Renforcement de la sécurité des comptes administrateurs Microsoft 365**

Microsoft rendra obligatoire l'authentification multifacteur (MFA) pour tous les accès au centre d'administration Microsoft 365 à partir du 9 février 2026. Cette mesure vise à renforcer considérablement la sécurité des comptes, rendant plus difficile pour les cybercriminels de s'emparer des identités. Cette nouvelle politique s'appliquera aux portails admin.microsoft.com, portal.office.com/adminportal/home et admin.cloud.microsoft.

**Points clés :**

*   **Date d'application :** 9 février 2026.
*   **Impact :** Tous les utilisateurs accédant au centre d'administration Microsoft 365 devront utiliser la MFA. Ceux qui n'auront pas activé la MFA seront bloqués.
*   **Objectif :** Protéger contre les attaques par hameçonnage, credential stuffing, attaques par force brute et réutilisation de mots de passe.
*   **Efficacité prouvée :** Une étude Microsoft de novembre 2023 indique que 99,99 % des comptes protégés par MFA bloquent les tentatives de piratage et réduisent le risque de compromission de compte de 98,56 %.
*   **Mesures antérieures :** La MFA est déjà obligatoire pour les connexions au portail Azure depuis mars 2025 et pour les interfaces de ligne de commande, PowerShell, SDK et API Azure depuis octobre 2025.

**Vulnérabilités (implicites) :**

Bien qu'aucun CVE spécifique ne soit mentionné, le renforcement de la MFA vise à pallier les vulnérabilités associées aux méthodes d'authentification faibles, telles que :

*   Hameçonnage (Phishing)
*   Credential stuffing (utilisation d'identifiants volés sur plusieurs plateformes)
*   Attaques par force brute
*   Réutilisation de mots de passe

**Recommandations :**

*   **Action immédiate :** Les administrateurs doivent configurer la MFA pour tous les utilisateurs avant la date limite pour éviter toute interruption des opérations informatiques.
*   **Configuration :** Les administrateurs globaux peuvent utiliser l'assistant de configuration de Microsoft ou la documentation officielle.
*   **Vérification individuelle :** Les utilisateurs peuvent vérifier et ajouter leurs méthodes d'authentification via le portail de configuration MFA de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-enforce-mfa-for-microsoft-365-admin-center-sign-ins/){:target="_blank"}
