---
title: 'MuddyWater Launches RustyWater RAT via Spear-Phishing Across Middle East Sectors'
date: 2026-01-10
permalink: /posts/2026/01/10/muddywater-launches-rustywater-rat-via-spear-phishing-across-middle-east-sectors/
tags:
- veille-cyber
- hackernews
---
## RustyWater : Nouvelle menace d'espionnage iranien

Un acteur de menace connu sous le nom de MuddyWater, présumé affilié au ministère iranien de la Sécurité et du Renseignement, a lancé une campagne de phishing ciblée dans le Moyen-Orient. Les secteurs diplomatique, maritime, financier et des télécommunications sont visés.

L'attaque utilise des documents Word malveillants, déguisés en directives de cybersécurité, qui incitent les victimes à activer le contenu. Ceci déclenche une macro VBA pour déployer un implant basé sur le langage de programmation Rust, baptisé RustyWater.

Ce logiciel malveillant, également connu sous les noms d'Archer RAT et RUSTRIC, est capable de recueillir des informations sur la machine victime, de détecter les logiciels de sécurité installés, d'établir une persistance via une clé de registre Windows et de communiquer avec un serveur de commande et contrôle ("nomercys.it[.]com") pour exécuter des commandes et gérer des fichiers.

RustyWater représente une évolution notable dans la boîte à outils de MuddyWater, passant de chargeurs PowerShell et VBS à des implants Rust plus structurés, modulaires et discrets, offrant des capacités d'accès à distance améliorées et une meilleure furtivité. L'utilisation de RUSTRIC a également été signalée dans des attaques visant des entreprises de technologies de l'information, des prestataires de services gérés, des ressources humaines et des sociétés de développement logiciel en Israël.

### Points Clés :

*   **Acteur de menace :** MuddyWater (également connu sous les noms de Mango Sandstorm, Static Kitten, TA450, affilié présumé au MOIS iranien).
*   **Campagne :** Spear-phishing ciblant des entités au Moyen-Orient (secteurs diplomatique, maritime, financier, télécoms).
*   **Vecteur d'infection :** Emails de spear-phishing contenant des documents Word malveillants.
*   **Logiciel malveillant :** RustyWater (implant basé sur Rust, RAT).
*   **Fonctionnalités de RustyWater :** Collecte d'informations, détection de sécurité, persistance (clé de registre), communication C2, exécution de commandes, opérations sur fichiers, capacités anti-analyse.
*   **Évolution des tactiques :** Passage de chargeurs PowerShell/VBS à des implants Rust personnalisés pour plus de discrétion et de modularité.

### Vulnérabilités :

L'article ne mentionne pas de CVE spécifiques exploitées pour l'installation initiale ou la persistance. L'attaque repose sur l'ingénierie sociale (incitant l'utilisateur à activer le contenu d'un document) et le déploiement d'un implant.

### Recommandations :

*   **Sensibilisation :** Renforcer la vigilance des employés face aux emails de phishing, en particulier ceux demandant d'activer le contenu des documents.
*   **Protection :** Maintenir les logiciels antivirus et les systèmes de détection d'intrusion à jour.
*   **Gestion des accès :** Vérifier les permissions d'accès et les configurations de registre pour détecter toute modification suspecte.
*   **Surveillance :** Mettre en place une surveillance continue des communications réseau pour identifier les interactions avec des serveurs de commande et contrôle potentiels.
*   **Analyse des logs :** Examiner les journaux d'événements pour identifier les activités malveillantes liées à l'exécution de macros et aux modifications du registre.

---
[Source](https://thehackernews.com/2026/01/muddywater-launches-rustywater-rat-via.html){:target="_blank"}
