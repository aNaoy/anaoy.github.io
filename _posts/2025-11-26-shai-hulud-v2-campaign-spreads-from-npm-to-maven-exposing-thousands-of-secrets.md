---
title: 'Shai-Hulud v2 Campaign Spreads From npm to Maven, Exposing Thousands of Secrets'
date: 2025-11-26
permalink: /posts/2025/11/26/shai-hulud-v2-campaign-spreads-from-npm-to-maven-exposing-thousands-of-secrets/
tags:
- veille-cyber
- hackernews
---
**Shai-Hulud v2 : Une Nouvelle Vague d'Attaques de la Chaîne d'Approvisionnement Logicielle**

La campagne Shai-Hulud v2, une attaque sophistiquée de la chaîne d'approvisionnement logicielle, s'étend désormais à l'écosystème Maven après avoir précédemment compromis des centaines de packages npm. Cette nouvelle itération vise à dérober des informations sensibles telles que des clés API, des identifiants cloud et des jetons npm/GitHub, tout en facilitant une compromission plus profonde de manière virale.

**Points Clés :**

*   **Étendue de l'Attaque :** Initialement focalisée sur npm, l'attaque s'est propagée à Maven via un package org.mvnpm:posthog-node:4.18.1, reconstruit à partir de composants npm compromis. Plus de 28 000 dépôts ont été touchés au total.
*   **Méthodologie :** Les attaquants obtiennent un accès non autorisé aux comptes de mainteneurs de packages, publient des versions infectées qui, une fois téléchargées, installent des backdoors et exfiltrent des secrets vers des dépôts GitHub.
*   **Techniques Évoluées :** La campagne v2 utilise le runtime Bun pour masquer sa logique, augmente le nombre de packages infectables, et exfiltre les données vers des dépôts GitHub nommés aléatoirement pour une discrétion accrue. Elle peut également avoir un comportement destructeur en dernier recours.
*   **Exploitation de Vulnérabilités :** Les attaquants exploitent des mauvaises configurations dans les workflows GitHub Actions, notamment les triggers `pull_request_target` et `workflow_run`, permettant l'exécution de code arbitraire lors des exécutions CI/CD.

**Vulnérabilités :**

*   Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, l'attaque exploite les mauvaises configurations des workflows GitHub Actions, spécifiquement le trigger `pull_request_target` dans les contextes `pull_request_target` et `workflow_run`. Cette mauvaise configuration permet l'exécution de code malveillant injecté dans les pull requests.

**Recommandations :**

*   **Rotation des Identifiants :** Révéler tous les jetons et clés compromis.
*   **Audit des Dépendances :** Examiner attentivement toutes les dépendances utilisées.
*   **Nettoyage des Packages :** Supprimer les versions compromises et réinstaller des packages sains.
*   **Sécurisation des Environnements :** Renforcer les environnements de développement et les systèmes CI/CD avec des principes de moindre privilège, des analyses de secrets et des politiques automatisées.
*   **Changement Fondamental :** Repenser la manière dont les logiciels sont construits, publiés et consommés pour renforcer la sécurité de la chaîne d'approvisionnement logicielle.

---
[Source](https://thehackernews.com/2025/11/shai-hulud-v2-campaign-spreads-from-npm.html){:target="_blank"}
