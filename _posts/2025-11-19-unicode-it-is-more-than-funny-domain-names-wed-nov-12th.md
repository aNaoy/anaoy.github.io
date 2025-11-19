---
title: 'Unicode: It is more than funny domain names., (Wed, Nov 12th)'
date: 2025-11-19
permalink: /posts/2025/11/19/unicode-it-is-more-than-funny-domain-names-wed-nov-12th/
tags:
- veille-cyber
- sans-isc
---
**Risques de sécurité Unicode au-delà des noms de domaine**

L'Unicode, bien plus qu'une simple gestion des noms de domaine internationaux, présente plusieurs vulnérabilités de sécurité souvent négligées.

**Points Clés :**

*   L'Unicode étend l'ASCII avec un nombre quasi illimité de caractères, incluant des emojis et symboles mathématiques.
*   Les problèmes de sécurité ne se limitent pas aux noms de domaine mais affectent l'authentification des utilisateurs, les filtres d'injection et l'exécution de code.

**Vulnérabilités :**

*   **Caractères "Confusables" :** Des caractères visuellement similaires peuvent être utilisés pour usurper l'identité d'un utilisateur sur des plateformes, comme observé sur X.
*   **Normalisation et Mappage "Best Fit" :** Des conversions de caractères non intentionnelles, visant à compenser les limites de certains systèmes, peuvent contourner les filtres de sécurité en transformant des caractères anodins en caractères interprétés comme des injections (ex: "FULLWIDTH GRAVE ACCENT" en apostrophe).
*   **Sélecteurs de Variante :** Des points de code Unicode non imprimables (ex: `#FE0F` pour les emojis) peuvent être utilisés pour dissimuler du code malveillant, comme dans l'attaque "Glass Worm" visant les extensions VS Code. Ces sélecteurs peuvent être abusés en séquences non conformes sans glyphe associé.
*   **Direction du Texte :** Les marques de direction (gauche-à-droite ou droite-à-gauche) peuvent être exploitées pour rendre le code source trompeur lors des revues humaines, tandis que les compilateurs ou interpréteurs l'exécutent différemment. L'exemple de trojansource.codes illustre ce risque.

**Recommandations :**

*   Éviter toute conversion de chaîne de caractères après validation des entrées.
*   Être vigilant quant à l'usage de caractères visuellement similaires dans les identifiants utilisateurs.
*   Contrôler l'utilisation des sélecteurs de variante, en particulier dans les contextes où du code peut être exécuté.
*   Appliquer une analyse rigoureuse des différences d'interprétation dues aux marques de direction du texte, notamment lors des revues de code.

---
[Source](https://isc.sans.edu/diary/rss/32472){:target="_blank"}
