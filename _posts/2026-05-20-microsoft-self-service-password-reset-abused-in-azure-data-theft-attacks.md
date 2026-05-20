---
title: 'Microsoft Self-Service Password Reset abused in Azure data theft attacks'
date: 2026-05-20
permalink: /posts/2026/05/20/microsoft-self-service-password-reset-abused-in-azure-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation des fonctionnalités Microsoft par le groupe Storm-2949

Le groupe de cybermenaces « Storm-2949 » cible les environnements Microsoft 365 et Azure en détournant des fonctionnalités administratives légitimes pour exfiltrer des données sensibles. Les attaquants utilisent l'ingénierie sociale pour obtenir les identifiants d'utilisateurs privilégiés, puis exploitent les outils de gestion du cloud pour maintenir leur accès et étendre leur compromission.

**Points clés :**
*   **Vecteur initial :** Manipulation du processus de réinitialisation de mot de passe en libre-service (SSPR) et usurpation d'identité auprès du support informatique pour valider des invites MFA.
*   **Mouvement latéral :** Utilisation de scripts Python et de l'API Microsoft Graph pour énumérer les accès, suivie d'une recherche ciblée de configurations VPN et de données opérationnelles dans OneDrive et SharePoint.
*   **Escalade dans Azure :** Exploitation des permissions RBAC pour accéder aux Key Vaults (vol de secrets), modifier les règles de pare-feu SQL/Storage et déployer des outils d'administration à distance (Kudu, ScreenConnect) sur des machines virtuelles.
*   **Dissimulation :** Tentatives de désactivation de Microsoft Defender et suppression de preuves forensiques.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, l'attaque repose sur l'abus de fonctionnalités légitimes et l'exploitation de l'erreur humaine (ingénierie sociale).

**Recommandations :**
*   **Authentification :** Imposer une MFA résistante au phishing pour tous les comptes à hauts privilèges.
*   **Gestion des accès :** Appliquer rigoureusement le principe du moindre privilège pour les rôles Azure RBAC et limiter strictement l'accès aux Key Vaults.
*   **Sécurité des données :** Restreindre l'accès public aux ressources Azure, conserver les journaux d'audit sur une longue période (au moins un an) et surveiller activement les opérations de gestion Azure à haut risque.
*   **Protection :** Mettre en œuvre des politiques d'accès conditionnel et auditer régulièrement les configurations de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-self-service-password-reset-abused-in-azure-data-theft-attacks/){:target="_blank"}
