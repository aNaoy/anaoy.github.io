---
title: 'ConnectWise Suspends Cloud Backup After Attackers Compromise Microsoft 365 Tenants'
date: 2026-10-18
permalink: /posts/2026/10/18/connectwise-suspends-cloud-backup-after-attackers-compromise-microsoft-365-tenants/
tags:
- veille-cyber
- hackernews
---
### Incident de sécurité : Compromission des identités ConnectWise et accès aux tenants Microsoft 365

ConnectWise a suspendu ses services de sauvegarde et de gestion cloud après la compromission d'identités d'applications. Des attaquants ont détourné ces accès privilégiés pour s'introduire dans des environnements Microsoft 365 clients, sans nécessiter les mots de passe individuels des utilisateurs.

**Points clés :**
*   **Mode opératoire :** L'utilisation des identités d'application compromises a permis aux attaquants d'obtenir des jetons d'accès via Microsoft Entra ID. Cette méthode autorise une élévation de privilèges (ajout de rôles d'administrateur global, création de nouvelles applications ou ajout de secrets clients pour maintenir une persistance).
*   **Services touchés :** Les services *Cloud Backup*, *Cloud Management*, ainsi que l'accès aux données via Exchange, SharePoint, Teams et Microsoft Graph sont concernés.
*   **Réponse de l'éditeur :** ConnectWise a désactivé sept identités d'application et suspendu temporairement ses outils SaaS. Les archives de sauvegarde restent chiffrées et isolées sans preuve d'accès malveillant à ce jour.
*   **Enquête en cours :** L'origine de la fuite des identifiants (vulnérabilité produit ou autre) n'est pas encore établie. Des tentatives ciblées ont été observées depuis l'adresse IP `144.172.64.128`.

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été publiée à ce stade. La faille réside dans l'exploitation abusive des autorisations accordées aux applications tierces au sein d'Entra ID.

**Recommandations pour les administrateurs :**
*   **Audit immédiat :** Inspecter les journaux de connexion de tous les tenants gérés depuis le 13 octobre 2026, en recherchant spécifiquement toute activité liée à l'IP `144.172.64.128`.
*   **Contrôle des accès :** Vérifier les nouvelles applications, les secrets clients ajoutés, les rôles d'annuaire modifiés et les règles de transfert de messagerie suspectes.
*   **Durcissement :** 
    *   Restreindre la création de secrets clients via les politiques de gestion des applications.
    *   Limiter le nombre d'utilisateurs ayant les rôles "Administrateur d'application".
    *   Mettre en œuvre des accès conditionnels pour les identités de charge de travail (*Workload Identities*) et surveiller les principaux de service via Microsoft Entra ID Protection.
*   **Maintien de la vigilance :** Maintenir la désactivation des applications ConnectWise impactées jusqu'à nouvel ordre et valider l'intégrité des environnements (y compris les connexions dormantes, ex: SkyKick).

---
[Source](https://thehackernews.com/2026/10/connectwise-suspends-cloud-backup-after.html){:target="_blank"}
