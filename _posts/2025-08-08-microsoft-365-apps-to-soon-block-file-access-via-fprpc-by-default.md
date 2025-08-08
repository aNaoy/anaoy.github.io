---
title: 'Microsoft 365 apps to soon block file access via FPRPC by default'
date: 2025-08-08
permalink: /posts/2025/08/08/microsoft-365-apps-to-soon-block-file-access-via-fprpc-by-default/
tags:
- veille-cyber
- bleepingcomp
---
**Renforcement de la sécurité pour l'accès aux fichiers dans Microsoft 365**

Microsoft va par défaut bloquer l'accès aux fichiers via le protocole d'authentification hérité FPRPC dans les applications Microsoft 365 pour Windows à partir de la fin août. Cette mesure vise à renforcer la sécurité en réduisant l'exposition aux technologies obsolètes telles que FPRPC (FrontPage Remote Procedure Call), FTP et HTTP.

**Points clés :**

*   **Blocage par défaut de FPRPC :** À partir de la version 2508 des applications Microsoft 365 pour Windows, les ouvertures de fichiers utilisant le protocole FPRPC seront bloquées par défaut. Elles seront remplacées par un protocole de repli plus sécurisé.
*   **Disponibilité :** Les changements seront généralement disponibles fin août 2025, avec une disponibilité pour tous les locataires d'ici fin septembre.
*   **Paramètres de gestion :** De nouveaux paramètres dans le Centre de gestion permettront aux utilisateurs de réactiver FPRPC, sauf si cela est géré par une stratégie de groupe ou le service de stratégie cloud (CPS). Il sera également possible de désactiver les ouvertures de fichiers FTP et HTTP, qui restent autorisées par défaut.
*   **Contrôle par les administrateurs :** Les administrateurs pourront gérer les paramètres des protocoles d'authentification via le service de stratégie cloud (CPS). Si un protocole est désactivé via CPS, les utilisateurs ne pourront pas le réactiver via le Centre de gestion.
*   **Contexte :** Cette initiative fait suite à une annonce précédente de Microsoft visant à bloquer l'accès aux fichiers via des protocoles d'authentification hérités pour se protéger contre les attaques par force brute et de phishing exploitant des méthodes d'authentification obsolètes.

**Vulnérabilités (non spécifiées avec CVE dans l'article) :**

*   Utilisation de protocoles d'authentification hérités considérés comme non sécurisés (FPRPC, FTP, HTTP).

**Recommandations :**

*   Les utilisateurs et administrateurs doivent se familiariser avec les nouveaux paramètres du Centre de gestion pour ajuster le blocage des protocoles si nécessaire.
*   Les administrateurs doivent utiliser le service de stratégie cloud (CPS) pour gérer ces paramètres de manière centralisée.
*   Se tenir informé des futures mises à jour de sécurité de Microsoft 365 pour garantir une protection optimale.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-365-apps-to-soon-block-file-access-via-insecure-fprpc-legacy-auth-protocol-by-default/){:target="_blank"}
