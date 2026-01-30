---
title: 'Researchers Uncover Chrome Extensions Abusing Affiliate Links and Stealing ChatGPT Access'
date: 2026-01-30
permalink: /posts/2026/01/30/researchers-uncover-chrome-extensions-abusing-affiliate-links-and-stealing-chatgpt-access/
tags:
- veille-cyber
- hackernews
---
### Extensions Malveillantes sur Chrome : Dérobage de Liens d'Affiliation et d'Accès à ChatGPT

Des extensions malveillantes ont été découvertes dans le Chrome Web Store, conçues pour détourner les liens d'affiliation, voler des données et subtiliser les jetons d'authentification pour OpenAI ChatGPT.

Une des extensions, "Amazon Ads Blocker", prétend bloquer les publicités sur Amazon, mais en réalité, elle injecte discrètement le tag d'affiliation de son développeur dans tous les liens de produits Amazon et remplace ceux existants. Cette pratique, qui affecte 29 extensions ciblant diverses plateformes de commerce électronique comme AliExpress, Amazon, et Walmart, viole les politiques du Chrome Web Store. Les développeurs de contenu perdent ainsi leurs commissions.

D'autres extensions, telles que "Good Tab", "Children Protection" et "DPS Websafe", collectent des données sensibles comme le contenu du presse-papiers, des cookies, et détournent les recherches des utilisateurs. Une vulnérabilité CVE-2020-28707 a été identifiée dans l'extension "Stock Informer", permettant l'exécution de code JavaScript arbitraire.

Un autre groupe de 16 extensions, se faisant passer pour des outils liés à ChatGPT, a été conçu pour intercepter et voler les jetons d'authentification de ChatGPT. La possession de ces jetons permettrait aux attaquants d'accéder aux conversations, données et codes des utilisateurs.

Ces découvertes coïncident avec l'apparition d'un kit malveillant appelé "Stanley", qui permettait de créer des extensions Chrome trompeuses conçues pour afficher des pages de phishing dans des iframes, tout en conservant l'URL légitime dans la barre d'adresse. Bien que ce service semble avoir disparu, le risque de réapparition demeure. L'utilisation croissante du navigateur comme point d'entrée pour des attaques est soulignée, rendant les extensions malveillantes un vecteur d'attaque majeur.

**Points Clés :**

*   **Détournement de Liens d'Affiliation :** Des extensions remplacent les tags d'affiliation existants par ceux des développeurs malveillants, privant les créateurs de contenu de leurs revenus.
*   **Vol de Jetons ChatGPT :** Un ensemble d'extensions dérobe les identifiants d'accès à ChatGPT, permettant l'usurpation d'identité et l'accès aux conversations.
*   **Collecte de Données Sensibles :** D'autres extensions volent des informations du presse-papiers, des cookies et des termes de recherche.
*   **Ingénierie Sociale :** Des techniques comme les fausses annonces de "deal limité dans le temps" et les iframes de phishing dissimulées derrière des URLs légitimes sont utilisées pour tromper les utilisateurs.
*   **Évolution des Vecteurs d'Attaque :** Le navigateur est de plus en plus considéré comme un point d'accès principal pour les cyberattaquants.

**Vulnérabilités (avec CVE si possible) :**

*   **CVE-2020-28707 :** Vulnérabilité XSS dans le plugin Stockdio Historical Chart pour WordPress, affectant potentiellement l'extension "Stock Informer". Score CVSS : 6.1.

**Recommandations :**

*   **Prudence lors de l'installation d'extensions :** Vérifier attentivement les permissions demandées et la réputation des développeurs, même en provenance de sources apparemment fiables.
*   **Surveiller les révélations des extensions :** S'assurer que la description et le comportement réel de l'extension correspondent.
*   **Privilégier les extensions à fonction unique :** Les extensions combinant plusieurs fonctionnalités non liées devraient être considérées avec prudence.
*   **Maintenir les navigateurs et extensions à jour :** Bien que non explicitement mentionné pour ces cas spécifiques, c'est une bonne pratique générale.
*   **Être vigilant face aux offres trop belles pour être vraies :** Les "deals" ou les outils gratuits promettant des fonctionnalités avancées doivent être examinés avec scepticisme.

---
[Source](https://thehackernews.com/2026/01/researchers-uncover-chrome-extensions.html){:target="_blank"}
