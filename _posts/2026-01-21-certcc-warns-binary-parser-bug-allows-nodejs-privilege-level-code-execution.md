---
title: 'CERT/CC Warns binary-parser Bug Allows Node.js Privilege-Level Code Execution'
date: 2026-01-21
permalink: /posts/2026/01/21/certcc-warns-binary-parser-bug-allows-nodejs-privilege-level-code-execution/
tags:
- veille-cyber
- hackernews
---
### Exécution de code arbitraire dans Node.js via la bibliothèque binary-parser

Une faille de sécurité a été découverte dans la bibliothèque npm `binary-parser`, permettant potentiellement l'exécution de code JavaScript arbitraire.

**Points Clés:**

*   La vulnérabilité affecte les versions de `binary-parser` antérieures à la version 2.3.0.
*   La bibliothèque génère du code JavaScript pour l'analyse de données binaires, en utilisant le constructeur `Function` pour créer et mettre en cache des fonctions d'analyse performantes.
*   Le problème réside dans le manque de validation des entrées fournies par l'utilisateur (noms de champs de parseur, paramètres d'encodage) lors de la génération dynamique de ce code.
*   Une entrée contrôlée par un attaquant peut être insérée dans le code généré, menant à l'exécution de code arbitraire avec les privilèges du processus Node.js.
*   Les applications utilisant uniquement des définitions de parseur statiques et codées en dur ne sont pas affectées.

**Vulnérabilités:**

*   **CVE-2026-1245** (score CVSS : non spécifié)

**Recommandations:**

*   Mettre à jour la bibliothèque `binary-parser` vers la version 2.3.0 ou une version ultérieure.
*   Éviter de passer des valeurs contrôlées par l'utilisateur dans les noms de champs de parseur ou les paramètres d'encodage.

---
[Source](https://thehackernews.com/2026/01/certcc-warns-binary-parser-bug-allows.html){:target="_blank"}
