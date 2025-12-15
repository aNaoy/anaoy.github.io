---
title: 'A Browser Extension Risk Guide After the ShadyPanda Campaign'
date: 2025-12-15
permalink: /posts/2025/12/15/a-browser-extension-risk-guide-after-the-shadypanda-campaign/
tags:
- veille-cyber
- hackernews
---
**L'ombre des extensions de navigateur : une menace subtile pour la sécurité SaaS**

Une campagne malveillante, baptisée ShadyPanda, a exploité pendant sept ans des extensions de navigateur Chrome et Edge populaires pour infecter environ 4,3 millions d'utilisateurs. Les attaquants ont d'abord publié des extensions légitimes, gagnant la confiance des utilisateurs avant de les transformer silencieusement en outils d'espionnage et de porte dérobée via des mises à jour automatiques. Ces extensions compromises pouvaient exécuter du code arbitraire, voler des données de navigation, des identifiants et, de manière critique, des jetons de session, permettant ainsi d'usurper l'identité des utilisateurs sur des services SaaS tels que Microsoft 365 ou Google Workspace.

**Points clés :**

*   **Attaque de la chaîne d'approvisionnement des extensions :** Des extensions initialement bénignes deviennent malveillantes après des mises à jour silencieuses.
*   **Longévité et confiance :** Les extensions étaient développées sur une longue période pour établir la confiance avant l'exploitation.
*   **Impact sur la sécurité SaaS :** Le vol de jetons de session contourne les authentifications multi-facteurs (MFA) en se basant sur des sessions déjà authentifiées.
*   **Élargissement de la surface d'attaque :** Les extensions transforment le navigateur en une extension de la surface d'attaque des applications SaaS.

**Vulnérabilités :**

Bien que des CVE spécifiques ne soient pas mentionnés pour les extensions elles-mêmes, la campagne exploite la confiance accordée aux extensions et la nature des mises à jour automatiques des navigateurs. La capacité principale exploitée est la **Capture de jetons de session et d'authentification**, permettant l'usurpation d'identité sur les services web.

**Recommandations :**

*   **Mettre en place des listes blanches d'extensions :** Restreindre l'installation aux seules extensions approuvées par l'équipe de sécurité, en traitant toutes les extensions comme potentiellement dangereuses jusqu'à preuve du contraire.
*   **Gérer l'accès des extensions comme l'accès OAuth :** Intégrer la gestion des extensions dans les processus de gestion des identités et des accès, en cartographiant les données et actions accessibles par chaque extension.
*   **Auditer régulièrement les permissions des extensions :** Examiner périodiquement les extensions installées et leurs permissions, en surveillant les changements de développeurs ou les demandes de permissions accrues.
*   **Surveiller les comportements suspects des extensions :** Mettre en place une surveillance technique (journaux, trafic réseau inhabituel) et sensibiliser les utilisateurs à signaler tout changement de comportement étrange.
*   **Traiter le navigateur comme une extension de la surface d'attaque SaaS :** Intégrer la gestion des extensions dans la stratégie globale de sécurité, en corrélant les risques côté navigateur avec le comportement des comptes SaaS.

---
[Source](https://thehackernews.com/2025/12/a-browser-extension-risk-guide-after.html){:target="_blank"}
