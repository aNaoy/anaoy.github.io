---
title: 'North Korean Hackers Publish 26 npm Packages Hiding Pastebin C2 for Cross-Platform RAT'
date: 2026-03-02
permalink: /posts/2026/03/02/north-korean-hackers-publish-26-npm-packages-hiding-pastebin-c2-for-cross-platform-rat/
tags:
- veille-cyber
- hackernews
---
## Steganographie sur Pastebin pour un RAT Cross-Platform

Des acteurs malveillants liés à la Corée du Nord, identifiés sous le nom de "Famous Chollima", ont propagé 26 paquets malveillants sur le registre npm. Ces paquets se présentent comme des outils pour développeurs mais dissimulent une fonctionnalité permettant d'extraire des URLs de commande et de contrôle (C2) via un système de stéganographie avancé. Les serveurs C2 sont hébergés sur Vercel.

La technique, baptisée "StegaBin", utilise des contenus apparemment anodins sur Pastebin (des essais sur l'informatique) pour cacher les adresses C2. Ces adresses sont encodées en modifiant des caractères à des positions précises dans le texte. Une fois extraites, ces URLs permettent de télécharger des charges utiles spécifiques à chaque plateforme (Windows, macOS, Linux) comprenant un RAT (Remote Access Trojan) et un voleur d'identifiants ciblant les développeurs.

Le RAT déployé permet un contrôle à distance du système infecté et l'exfiltration de données sensibles, notamment :
*   Des modules pour assurer la persistance dans VS Code.
*   Un enregistreur de frappe et un voleur de presse-papiers.
*   Le vol d'identifiants de navigateurs et de portefeuilles de cryptomonnaies.
*   L'utilisation de l'outil légitime "TruffleHog" pour la découverte de secrets.
*   L'exfiltration de clés SSH et de dépôts Git.

Cette campagne "Contagious Interview" démontre une évolution des techniques d'évasion des attaquants nord-coréens, visant à contourner les détections automatisées et l'examen humain.

**Points Clés :**

*   **26 paquets malveillants publiés sur npm.**
*   **Utilisation de stéganographie sur Pastebin pour masquer les adresses C2.**
*   **Infrastructure C2 hébergée sur Vercel.**
*   **Déploiement d'un RAT cross-platform et d'un voleur d'identifiants.**
*   **Ciblage des développeurs et de leurs environnements de développement.**

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article pour les paquets eux-mêmes, mais l'attaque exploite la confiance accordée aux paquets npm et la complexité de la détection des techniques de stéganographie.

**Recommandations :**

*   **Vigilance accrue lors de l'installation de paquets npm, en particulier ceux qui peuvent être des fautes de frappe de paquets légitimes.**
*   **Audit régulier des dépendances des projets pour identifier les paquets suspects.**
*   **Mise en place de solutions de sécurité capables de détecter des comportements anormaux lors de l'installation et de l'exécution de paquets.**
*   **Formation des développeurs aux risques liés à la chaîne d'approvisionnement logicielle.**

---
[Source](https://thehackernews.com/2026/03/north-korean-hackers-publish-26-npm.html){:target="_blank"}
