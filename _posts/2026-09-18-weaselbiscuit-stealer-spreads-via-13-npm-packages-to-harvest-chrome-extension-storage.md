---
title: 'WeaselBiscuit Stealer Spreads via 13 npm Packages to Harvest Chrome Extension Storage'
date: 2026-09-18
permalink: /posts/2026/09/18/weaselbiscuit-stealer-spreads-via-13-npm-packages-to-harvest-chrome-extension-storage/
tags:
- veille-cyber
- hackernews
---
### Menace émergente : Le voleur de données WeaselBiscuit sur npm

Des chercheurs en cybersécurité ont identifié 13 paquets malveillants sur le registre **npm** diffusant un nouveau logiciel malveillant baptisé **WeaselBiscuit**. Ce "stealer" JavaScript se distingue par sa légèreté et sa simplicité, tout en partageant des similitudes fonctionnelles avec les souches *BeaverTail* et *OtterCookie*, souvent associées à des campagnes liées à la Corée du Nord.

#### Points clés
*   **Mode opératoire :** Le malware est activé par un simple `import` npm, déclenchant le téléchargement et l'exécution en mémoire d'une charge utile hébergée sur Npoint.
*   **Objectif :** Exfiltration des données stockées dans les extensions Chrome (fichiers LevelDB). Sur Windows, il peut également capturer le contenu du presse-papier et enregistrer les frappes clavier.
*   **Architecture :** Contrairement à ses prédécesseurs, il est dépourvu de fonctionnalités de persistance, d'accès à distance ou de vidage de portefeuilles crypto directs, se concentrant exclusivement sur l'exfiltration de données sensibles issues des extensions de navigateur.
*   **Infrastructure :** Utilise des services légers (Npoint.io) pour la configuration C2 et le stockage de données. Le serveur de commande et contrôle identifié est `103.170.217[.]184:8787`.
*   **Attribution :** Bien que des indices techniques (méthodes d'hébergement, architecture C2, convention de nommage par ID) pointent vers des acteurs nord-coréens, aucune preuve définitive ne permet à ce jour une attribution formelle.

#### Vulnérabilités ciblées
*   Il n'existe pas de CVE spécifique, car il s'agit d'une attaque par **supply chain (chaîne d'approvisionnement)** visant les développeurs via des dépendances npm piégées.
*   **Impact :** Vol de jetons de session, clés privées ou données sensibles conservées par les extensions de navigateur (notamment les portefeuilles Web3).

#### Paquets compromis
*   `@biz44/id10-client`, `@biz44/id12-client`, `@biz44/id44-client`, `@biz44/id79-client`, `@biz44/id95-client`, `@biz44/id99-client`
*   `@biz44/process-runtime-utils`, `@biz44/runtime-utils`
*   `engin1`, `id79-client`, `process-lhpm`, `process-mite`, `process-tailwind`

#### Recommandations
*   **Audit des dépendances :** Vérifiez et nettoyez immédiatement vos projets npm pour supprimer les paquets listés ci-dessus.
*   **Gestion des accès :** Appliquez le principe du moindre privilège aux extensions de navigateur et révoquez les sessions si des outils de développement suspects ont été installés récemment.
*   **Surveillance réseau :** Bloquez le trafic sortant vers l'adresse IP `103.170.217.184` et surveillez les appels vers `Npoint.io` au sein de vos applications.
*   **Vigilance :** Exercez une grande prudence lors de l'installation de nouveaux paquets npm, en particulier ceux provenant de sources inconnues ou utilisant des noms trompeurs.

---
[Source](https://thehackernews.com/2026/09/weaselbiscuit-stealer-spreads-via-13.html){:target="_blank"}
