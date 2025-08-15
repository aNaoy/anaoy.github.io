---
title: 'Trojans Embedded in .svg Files'
date: 2025-08-15
permalink: /posts/2025/08/15/trojans-embedded-in-svg-files/
tags:
- veille-cyber
- schneier
---
**Dangers Cachés dans les Fichiers SVG : Une Menace Discrète**

Des sites web, notamment ceux à contenu pour adultes, exploitent des fichiers au format SVG (Scalable Vector Graphics) pour dissimuler des codes malveillants. Ces scripts JavaScript, souvent fortement obfusqués à l'aide de techniques comme le "JSFuck", rendent leur analyse complexe. Une fois décodé, le code déclenche le téléchargement d'une chaîne de scripts obfusqués supplémentaires.

Le chargeur utile final, identifié comme Trojan.JS.Likejack, a pour fonction d'automatiser des actions sur Facebook, spécifiquement l'action de "J'aime" sur une publication ciblée. Ce mécanisme s'active à l'insu de l'utilisateur, tant que celui-ci est connecté à son compte Facebook dans son navigateur. Bien que la présence de ce type d'attaque ne soit pas nouvelle, la méthode continue d'être utilisée pour manipuler les interactions sur les plateformes sociales.

**Points Clés :**

*   Utilisation de fichiers SVG pour dissimuler du code malveillant.
*   Obfuscation avancée du JavaScript pour rendre le code difficile à analyser.
*   Exploitation de la connexion active des utilisateurs à Facebook.
*   Automatisation non autorisée d'actions ("J'aime") sur des publications.

**Vulnérabilités :**

L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. La menace réside dans l'interprétation des fichiers SVG par les navigateurs, qui peuvent exécuter le code JavaScript embarqué.

**Recommandations :**

Bien que l'article ne détaille pas explicitement les recommandations, il est implicite que la prudence accrue lors de la navigation sur des sites potentiellement à risque est essentielle. De plus, maintenir des pratiques de sécurité strictes pour les comptes en ligne, comme la déconnexion lorsque l'accès n'est pas immédiat, peut atténuer ce risque. Une vigilance accrue quant aux interactions inattendues sur les plateformes sociales est également conseillée.

---
[Source](https://www.schneier.com/blog/archives/2025/08/trojans-embedded-in-svg-files.html){:target="_blank"}
