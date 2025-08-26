---
title: 'Inline Style Exfiltration: leaking data with chained CSS conditionals'
date: 2025-08-26
permalink: /posts/2025/08/26/inline-style-exfiltration-leaking-data-with-chained-css-conditionals/
tags:
- veille-cyber
- zerodaysfans
---
## Vol de Données via les Styles CSS En Ligne Conditionnels

Une nouvelle méthode permet d'exfiltrer des données à l'aide de styles CSS directement intégrés dans les balises HTML, sans nécessiter d'importation de feuilles de style externes. Cette technique exploite les fonctionnalités `attr()` et `image-set()` combinées aux nouvelles instructions `if` de CSS pour créer des requêtes réseau conditionnelles.

### Points Clés

*   Il est possible d'extraire des attributs HTML directement à l'aide de styles inline.
*   L'utilisation des fonctions `attr()` et `image-set()` permet de référencer la valeur d'un attribut et de l'utiliser pour déclencher une requête réseau, potentiellement vers un domaine contrôlé par l'attaquant.
*   Les instructions `if` dans le CSS permettent de conditionner ces requêtes en fonction de la valeur de l'attribut.
*   Des instructions `if` imbriquées peuvent être utilisées pour tester plusieurs valeurs d'attribut séquentiellement.
*   Cette technique est particulièrement efficace pour exfiltrer des données simples comme des identifiants ou des noms d'utilisateur.
*   Un outil personnalisé pour Burp Suite a été développé pour automatiser la recherche et l'exfiltration de ces données par force brute.
*   La technique est actuellement fonctionnelle sur les navigateurs basés sur Chromium.

### Vulnérabilités

*   **CSS Injection via Style Attributes:** La possibilité d'injecter du CSS directement dans les attributs `style` permet d'exécuter cette logique d'exfiltration. Aucun identifiant CVE spécifique n'est mentionné pour cette méthode d'exfiltration particulière, mais elle découle de l'interprétation des fonctionnalités CSS existantes.

### Recommandations

*   **Sensibilisation et Formation:** Informer les développeurs sur cette nouvelle méthode d'exfiltration et sur les risques potentiels.
*   **Sanitisation des Entrées:** Valider et nettoyer soigneusement toutes les entrées utilisateur qui pourraient être utilisées pour construire des attributs HTML ou des styles CSS.
*   **Contrôle de Contenu (Content Security Policy - CSP):** Mettre en place des politiques CSP restrictives pour limiter la possibilité de charger des ressources (comme des images via `image-set()`) à partir de domaines non autorisés.
*   **Tests de Sécurité Réguliers:** Effectuer des tests de sécurité approfondis, en particulier pour les applications web, afin de détecter de telles vulnérabilités.

---
[Source](https://portswigger.net/research/inline-style-exfiltration){:target="_blank"}
