---
title: 'Scalable Vector Grief'
date: 2026-10-27
permalink: /posts/2026/10/27/scalable-vector-grief/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilités critiques des désinfectants SVG

Cette recherche démontre que la majorité des bibliothèques de désinfection SVG sont vulnérables à des techniques de contournement avancées permettant l'exécution de code JavaScript (XSS).

**Points clés :**
*   **Confusion d'espaces de noms :** En basculant vers l'espace de noms XHTML (`xmlns="http://www.w3.org/1999/xhtml"`), il est possible d'injecter des éléments HTML actifs (ex: `<frame>`, `<iframe>`) directement dans un SVG.
*   **Contournement par animation :** L'utilisation de balises `<animate>` ou `<animateTransform>` permet de modifier dynamiquement les attributs d'un lien pour y injecter un schéma `javascript:`.
*   **XSLT et exécution de scripts :** L'injection d'une instruction `xml-stylesheet` pointant vers une URL de données (`data:text/xsl`) permet d'exécuter du JavaScript, même dans des fichiers XML apparemment inoffensifs.
*   **Attaque via en-tête HTTP :** Firefox peut exécuter des scripts via un en-tête `Link` contenant une feuille de style XSLT malveillante, ignorant la nature inoffensive du corps de la réponse.
*   **Importation d'images dans Safari :** Safari permet d'importer des fichiers image (comme des GIF) au sein d'un SVG via l'élément `<use>`, permettant d'exécuter des payloads cachés dans des fichiers non-SVG.

**Vulnérabilités :**
Aucun identifiant CVE spécifique n'est mentionné dans l'article, car ces failles concernent des défauts de logique dans les bibliothèques de traitement (notamment `mattkrick/sanitize-svg`, `Borewit/svg-sanitizer`, `bgalek/safe-svg`, `alnorris/SVG-Sanitizer`, `cloudflare/svg-hush` et `jams2/py-svg-hush`).

**Recommandations :**
*   **Utiliser des solutions robustes :** Privilégier des bibliothèques éprouvées comme **DOMPurify** ou `darylldoyle/svg-sanitizer`, qui ont résisté aux vecteurs d'attaque présentés.
*   **Strict filtering :** Les désinfectants doivent non seulement filtrer les balises, mais aussi valider les espaces de noms XML et bloquer les instructions de traitement (processing instructions) comme `xml-stylesheet`.
*   **Isolement :** Servir les fichiers SVG téléchargés par les utilisateurs depuis un domaine isolé (sandbox) pour limiter l'impact en cas de XSS.
*   **Politique de contenu :** Implémenter une politique de sécurité du contenu (CSP) stricte interdisant l'exécution de scripts inline et limitant les sources autorisées pour les ressources externes.

---
[Source](https://portswigger.net/research/scalable-vector-grief){:target="_blank"}
