---
title: 'Where Multi-Factor Authentication Stops and Credential Abuse Starts'
date: 2026-03-05
permalink: /posts/2026/03/05/where-multi-factor-authentication-stops-and-credential-abuse-starts/
tags:
- veille-cyber
- hackernews
---
### La Faille de la Protection par Mots de Passe dans les Environnements Windows

Malgré la mise en place de l'authentification multifacteur (MFA), les compromissions de comptes via des identifiants volés restent fréquentes dans les environnements Windows. La cause principale est le manque de couverture de la MFA, qui n'est souvent appliquée qu'aux applications cloud et aux connexions fédérées, laissant de nombreuses méthodes d'authentification Windows vulnérables.

**Points Clés :**

*   L'authentification directe sur les postes de travail Windows (logon interactif) utilise généralement Active Directory (AD) plutôt qu'un fournisseur d'identité cloud, contournant ainsi la MFA des applications SaaS.
*   Les protocoles d'authentification hérités comme NTLM, ainsi que les tickets Kerberos compromis (Golden Ticket, Silver Ticket), permettent aux attaquants de contourner les mesures de sécurité.
*   Les comptes administrateurs locaux et les comptes de service, souvent mal gérés, représentent des vecteurs d'attaque faciles pour l'escalade de privilèges et le mouvement latéral.
*   La réutilisation de mots de passe compromis issus de fuites de données est une tactique courante exploitée par les attaquants.

**Vulnérabilités et Vecteurs d'Attaque :**

*   **Authentification locale ou jointe au domaine Windows :** Les connexions directes à une machine Windows n'activent pas toujours la MFA, permettant l'utilisation de mots de passe ou de hachages volés.
*   **Accès RDP direct :** Les sessions RDP peuvent ne pas être soumises aux contrôles de MFA basés sur le cloud.
*   **Authentification NTLM :** Protocol d'authentification obsolète, vulnérable aux attaques de type "pass-the-hash".
*   **Abus de tickets Kerberos :** Exploitation de tickets Kerberos volés ou forgés pour un accès persistant et des mouvements latéraux.
*   **Comptes administrateurs locaux et réutilisation d'identifiants :** La compromission d'un compte admin local peut mener à une large diffusion sur le réseau.
*   **Authentification SMB :** Utilisée pour le partage de fichiers et le mouvement latéral, souvent sans MFA appliquée.
*   **Comptes de service :** Souvent dotés de privilèges élevés, de cycles de vie longs et difficiles à sécuriser avec la MFA.

**Recommandations :**

*   **Appliquer des politiques de mots de passe robustes dans AD :** Favoriser les phrases de passe longues (15+ caractères), interdire la réutilisation et bloquer les modèles faibles.
*   **Bloquer continuellement les mots de passe compromis :** Utiliser des bases de données de mots de passe divulgués pour empêcher leur utilisation lors de la création ou du changement de mot de passe.
*   **Réduire l'exposition aux protocoles d'authentification hérités :** Limiter ou éliminer l'utilisation de NTLM lorsque cela est possible.
*   **Auditer les comptes de service :** Inventorier ces comptes, réduire leurs privilèges au strict nécessaire, faire pivoter leurs identifiants et supprimer ceux qui ne sont plus utilisés.
*   **Étendre la MFA aux points d'accès Windows :** Mettre en œuvre la MFA pour les connexions interactives, RDP et VPN.
*   **Sécuriser les comptes administrateurs locaux :** Utiliser des mots de passe uniques et complexes, et envisager des solutions de gestion des identifiants à privilèges.

---
[Source](https://thehackernews.com/2026/03/where-multi-factor-authentication-stops.html){:target="_blank"}
