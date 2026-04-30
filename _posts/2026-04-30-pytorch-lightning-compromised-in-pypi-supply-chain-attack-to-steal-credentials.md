---
title: 'PyTorch Lightning Compromised in PyPI Supply Chain Attack to Steal Credentials'
date: 2026-04-30
permalink: /posts/2026/04/30/pytorch-lightning-compromised-in-pypi-supply-chain-attack-to-steal-credentials/
tags:
- veille-cyber
- hackernews
---
### Attaques par empoisonnement de la chaîne d'approvisionnement : Lightning et Intercom

Des attaquants ont compromis le célèbre package Python **Lightning** (versions 2.6.2 et 2.6.3) ainsi que le package npm **intercom-client** (version 7.0.4) dans le cadre de la campagne malveillante « Mini Shai-Hulud ». Cette opération vise le vol massif d'identifiants sur les systèmes des développeurs et au sein des environnements CI/CD.

**Points clés :**
* **Propagation automatique :** L'exécution du code malveillant est déclenchée automatiquement lors de l'importation ou de l'installation du module.
* **Mécanisme d'infection :** Les packages utilisent des scripts obfusqués pour télécharger et exécuter un runtime JavaScript (Bun) qui déploie une charge utile de vol de données.
* **Persistance et propagation :** Le malware injecte du code malveillant dans les dépôts GitHub accessibles via les jetons volés (type "ver") et modifie les fichiers `package.json` locaux pour infecter d'autres projets lors de leur publication sur npm.
* **Attribution :** Les activités sont liées au groupe « TeamPCP », en collaboration avec le groupe LAPSUS$.
* **Vecteur initial :** La compromission du compte GitHub du projet Lightning est fortement suspectée.

**Vulnérabilités :**
* Pas de CVE spécifique assignée, mais une compromission directe de l'intégrité logicielle via des injections de code malveillant dans le dépôt source/paquet distribué.

**Recommandations :**
* **Suppression :** Désinstaller immédiatement les versions compromises de Lightning (2.6.2, 2.6.3) et de `intercom-client` (7.0.4).
* **Mise à jour :** Rétrograder vers la dernière version connue comme saine (Lightning 2.6.1).
* **Remédiation des identifiants :** Procéder à une rotation immédiate de tous les secrets, jetons GitHub et clés d'API potentiellement exposés dans les environnements où ces packages ont été utilisés.
* **Audit :** Vérifier les commits récents des dépôts associés pour détecter des modifications non autorisées ou des tentatives d'injection de code.

---
[Source](https://thehackernews.com/2026/04/pytorch-lightning-compromised-in-pypi.html){:target="_blank"}
