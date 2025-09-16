---
title: 'Self-Replicating Worm Hits 180+ Software Packages'
date: 2025-09-16
permalink: /posts/2025/09/16/self-replicating-worm-hits-180-software-packages/
tags:
- veille-cyber
- krebs
---
**Shai-Hulud : Un ver auto-réplicatif s'attaque aux dépôts de code JavaScript**

Un ver malveillant nommé Shai-Hulud a infecté plus de 180 paquets du registre NPM (Node Package Manager), une plateforme essentielle pour le développement JavaScript. Ce ver a pour objectif de voler les identifiants (tokens NPM, clés SSH, clés API) des développeurs et de les publier sur des dépôts GitHub publics créés par les attaquants.

L'attaque tire parti des procédures d'installation de paquets NPM. Lorsqu'un développeur installe un paquet infecté, le ver recherche les tokens NPM dans son environnement. S'il en trouve, il se copie dans les 20 paquets les plus populaires auxquels ce token donne accès, publie une nouvelle version de ces paquets, propageant ainsi l'infection. Il utilise l'outil open-source TruffleHog pour rechercher les identifiants exposés sur la machine de la victime. Le ver semble cibler spécifiquement les environnements Linux et macOS, en omettant les systèmes Windows, et peut également exfiltrer des secrets AWS, Azure et Google Cloud Platform.

Cette campagne s'inscrit dans un contexte d'attaques croissantes visant la chaîne d'approvisionnement logicielle, notamment après une campagne de phishing récente visant à compromettre les authentifications multifactorielles des développeurs NPM.

**Points Clés :**

*   **Nature de l'attaque :** Ver auto-réplicatif ciblant le registre NPM.
*   **Objectif :** Vol et publication d'identifiants de développeurs sur GitHub.
*   **Cible :** Plus de 180 paquets NPM affectés, y compris certains de CrowdStrike.
*   **Mécanisme de propagation :** Exploitation des tokens NPM pour infecter d'autres paquets populaires maintenus par la même entité.
*   **Outils utilisés :** TruffleHog pour la reconnaissance, création de dépôts GitHub pour l'exfiltration.
*   **Environnements ciblés :** Linux et macOS, avec une exfiltration possible de secrets cloud.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques pour le ver Shai-Hulud. La vulnérabilité réside dans le modèle de publication actuel de NPM, qui permet des mises à jour automatisées sans consentement humain explicite pour chaque publication.

**Recommandations :**

*   **Pour les plateformes comme NPM :** Adopter un modèle de publication qui exige un consentement humain explicite, idéalement via une authentification à deux facteurs (2FA) résistante au phishing, pour chaque demande de publication. L'automatisation complète des mises à jour de paquets publiés est une "recette prouvée du désastre".
*   **Pour les développeurs :** Faire preuve de vigilance lors de l'installation de paquets. Surveiller l'activité des comptes de dépôt (comme GitHub) pour détecter toute création de dépôt suspecte ou publication d'informations sensibles. Révérer et remplacer les clés d'authentification si une compromission est suspectée.

---
[Source](https://krebsonsecurity.com/2025/09/self-replicating-worm-hits-180-software-packages/){:target="_blank"}
