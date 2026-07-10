---
title: 'Injective Labs GitHub Compromise Pushes Wallet-Key-Stealing npm Packages'
date: 2026-07-10
permalink: /posts/2026/07/10/injective-labs-github-compromise-pushes-wallet-key-stealing-npm-packages/
tags:
- veille-cyber
- hackernews
---
### Compromission de la supply chain npm : le SDK d'Injective Labs détourné

Une attaque par compromission de la chaîne d'approvisionnement logicielle a ciblé le SDK d'Injective Labs, permettant à des acteurs malveillants d'injecter du code dans le registre npm afin de dérober des clés privées et des phrases mnémoniques de portefeuilles de cryptomonnaies.

**Points clés :**
*   **Vecteur d'attaque :** Le compte GitHub d'un contributeur de confiance a été utilisé pour soumettre des commits malveillants, validés via le pipeline de publication sécurisé (OIDC).
*   **Propagation :** La version compromise (`@injectivelabs/sdk-ts@1.20.21`) a infecté 17 autres paquets dépendants, étendant la portée de l'attaque aux utilisateurs indirects.
*   **Mécanisme de vol :** Le code malveillant se dissimule sous la forme d'une fonction de télémétrie légitime (`trackKeyDerivation()`) censée optimiser les performances. En réalité, elle intercepte et exfiltre les informations sensibles vers un serveur distant.
*   **Discrétion :** Le malware évite les scripts de cycle de vie (installation) pour ne pas déclencher d'alertes et regroupe les données volées pour minimiser les requêtes réseau.

**Vulnérabilités :**
*   **CVE :** Aucune CVE spécifique n'est mentionnée, car il s'agit d'une compromission de compte et d'une injection de code malveillant intentionnel (malware supply chain) plutôt que d'une faille technique logicielle.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version saine (`1.20.23`) du paquet.
*   **Rotation des secrets :** Toute clé privée ou phrase mnémonique ayant été manipulée avec la version compromise du SDK doit être considérée comme compromise ; il est impératif de générer de nouveaux portefeuilles et de transférer les fonds.
*   **Audit des dépendances :** Vérifier les arbres de dépendances (y compris transitives) pour s'assurer qu'aucune version obsolète ou malveillante ne subsiste dans les environnements de développement et de production.

---
[Source](https://thehackernews.com/2026/07/injective-labs-github-compromise-pushes.html){:target="_blank"}
