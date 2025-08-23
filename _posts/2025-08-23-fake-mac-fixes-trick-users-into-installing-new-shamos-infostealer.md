---
title: 'Fake Mac fixes trick users into installing new Shamos infostealer'
date: 2025-08-23
permalink: /posts/2025/08/23/fake-mac-fixes-trick-users-into-installing-new-shamos-infostealer/
tags:
- veille-cyber
- bleepingcomp
---
**Shamos : La nouvelle menace furtive sur macOS**

Une nouvelle souche de logiciel malveillant, nommée Shamos, se propage actuellement sur les systèmes macOS. Développée par le groupe de cybercriminels "COOKIE SPIDER", elle se présente comme une variante d'Atomic macOS Stealer (AMOS) et vise à dérober des informations sensibles.

Les attaques, orchestrées via des techniques dites "ClickFix", trompent les utilisateurs en leur faisant croire qu'ils résolvent des problèmes système ou installent des correctifs. Ces manœuvres incitent les victimes à exécuter des commandes dans le Terminal macOS. Ces commandes, souvent diffusées via de la publicité malveillante ou de faux dépôts GitHub, téléchargent en réalité le malware.

Une fois installé, Shamos tente de déjouer les mesures de sécurité comme Gatekeeper en exploitant des commandes telles que `xattr` et `chmod`. Il procède ensuite à la collecte de données, incluant les identifiants de navigateurs web, les informations du Trousseau d'accès, les notes Apple et les données des portefeuilles de cryptomonnaies. Dans certains cas, il peut également installer des modules de botnet ou des applications de portefeuille falsifiées. Pour assurer sa persistance, Shamos peut créer des fichiers de lancement automatique s'il obtient des privilèges élevés.

**Points Clés :**

*   **Nature du malware :** Infostealer (voleur d'informations).
*   **Cible :** Systèmes macOS.
*   **Méthode de distribution :** Attaques "ClickFix" via publicités malveillantes et faux dépôts GitHub.
*   **Objectif :** Vol de données sensibles (identifiants, clés, cryptomonnaies).
*   **Auteur :** Groupe "COOKIE SPIDER".
*   **Variante de :** Atomic macOS Stealer (AMOS).
*   **Persistance :** Création de LaunchDaemons si les privilèges suffisants sont obtenus.
*   **Extensions de menace :** Téléchargement de charges utiles supplémentaires (botnet, fausses applications de portefeuille).

**Vulnérabilités exploitées (sans CVE spécifiques mentionnées dans l'article) :**

*   La confiance des utilisateurs dans les instructions trouvées en ligne.
*   La capacité à contourner Gatekeeper via des commandes spécifiques.
*   L'utilisation de scripts pour télécharger et exécuter du code malveillant.

**Recommandations :**

*   Ne jamais exécuter de commandes trouvées en ligne sans en comprendre pleinement l'objectif.
*   Se méfier des dépôts GitHub qui pourraient héberger des projets malveillants.
*   Privilégier les sources d'aide officielles et fiables pour résoudre les problèmes macOS, comme les forums communautaires Apple ou l'aide intégrée au système.
*   Éviter les résultats de recherche sponsorisés lorsqu'on cherche de l'aide pour des problèmes informatiques.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-mac-fixes-trick-users-into-installing-new-shamos-infostealer/){:target="_blank"}
