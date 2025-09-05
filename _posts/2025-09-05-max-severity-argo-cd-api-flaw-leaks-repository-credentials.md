---
title: 'Max severity Argo CD API flaw leaks repository credentials'
date: 2025-09-05
permalink: /posts/2025/09/05/max-severity-argo-cd-api-flaw-leaks-repository-credentials/
tags:
- veille-cyber
- bleepingcomp
---
**Faille critique dans Argo CD : fuite d'identifiants de dépôts**

Une faille de sécurité critique a été découverte dans Argo CD, un outil de déploiement continu et de GitOps largement utilisé par de grandes entreprises. Cette vulnérabilité permet à des attaquants, même avec des permissions limitées au niveau projet, d'accéder à des informations sensibles.

**Points Clés :**

*   La faille, identifiée sous **CVE-2025-55190**, est classée avec la sévérité maximale de 10.0 (CVSS v3).
*   Elle permet de contourner les mécanismes d'isolation conçus pour protéger les identifiants de dépôts (noms d'utilisateur, mots de passe).
*   Les attaquants possédant ces identifiants peuvent cloner des bases de code privées, injecter du code malveillant, ou compromettre d'autres ressources où les mêmes identifiants sont réutilisés.
*   La vulnérabilité affecte toutes les versions d'Argo CD jusqu'à la version 2.13.0.
*   La faille est accessible via des jetons d'API Argo CD, même si ceux-ci ne possèdent que des permissions standard de gestion d'applications ou des permissions globales de type "projects, get, *".

**Vulnérabilités :**

*   **CVE-2025-55190 :** Permet l'accès aux identifiants de dépôts (noms d'utilisateur, mots de passe) via le point d'accès API `project details` avec des permissions de lecture au niveau projet, même sans autorisation explicite sur les secrets.

**Recommandations :**

*   Mettre à jour Argo CD vers l'une des versions corrigées : 3.1.2, 3.0.14, 2.14.16, ou 2.13.9.
*   Veiller à ce que les jetons d'API disposent uniquement des permissions nécessaires et qu'ils n'aient pas un accès implicite ou explicite aux informations d'identification sensibles des dépôts.

---
[Source](https://www.bleepingcomputer.com/news/security/max-severity-argo-cd-api-flaw-leaks-repository-credentials/){:target="_blank"}
