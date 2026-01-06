---
title: 'Critical AdonisJS Bodyparser Flaw (CVSS 9.2) Enables Arbitrary File Write on Servers'
date: 2026-01-06
permalink: /posts/2026/01/06/critical-adonisjs-bodyparser-flaw-cvss-92-enables-arbitrary-file-write-on-servers/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilité Critique dans le Module Bodyparser d'AdonisJS**

Une faille de sécurité majeure a été découverte dans le package npm `@adonisjs/bodyparser`, permettant à un attaquant distant d'écrire des fichiers arbitraires sur un serveur. Identifiée sous la référence CVE-2026-21440 avec un score CVSS de 9.2, cette vulnérabilité concerne un problème de "path traversal" (traversée de chemin) dans la gestion des fichiers multipart de AdonisJS, un framework Node.js.

Le problème réside dans la fonction `MultipartFile.move()`. Si le paramètre `options` n'est pas fourni ou si le nom du fichier n'est pas correctement assaini, un attaquant peut injecter des séquences de traversée dans le nom du fichier. Cela permet d'écrire des fichiers en dehors du répertoire de téléchargement prévu, potentiellement sur des fichiers système sensibles. L'exécution de code à distance (RCE) devient possible si l'attaquant parvient à écraser des scripts de démarrage ou des fichiers de configuration.

Les versions affectées sont :
* Inférieures ou égales à 10.1.1 (corrigé dans 10.1.2)
* Inférieures ou égales à 11.0.0-next.5 (corrigé dans 11.0.0-next.6)

**Points Clés :**

*   **Vulnérabilité :** Traversée de chemin (Path Traversal) dans la gestion des fichiers multipart.
*   **Impact Potentiel :** Écriture arbitraire de fichiers sur le serveur, pouvant mener à l'exécution de code à distance.
*   **Cause :** Absence de validation ou d'assainissement du nom de fichier fourni par l'utilisateur lors du déplacement de fichiers via `MultipartFile.move()`.
*   **Conditions :** Nécessite un point d'accès au téléchargement de fichiers atteignable et potentiellement l'activation de l'écrasement de fichiers.

**Recommandations :**

*   Mettre à jour le package `@adonisjs/bodyparser` vers les versions corrigées (10.1.2 ou 11.0.0-next.6 et supérieures).
*   Lors de l'utilisation de `MultipartFile.move()`, toujours fournir le second argument `options` et s'assurer que le nom du fichier est correctement assaini.

*Article mentionne également une autre vulnérabilité similaire dans jsPDF (CVE-2025-68428), également corrigée.*

---
[Source](https://thehackernews.com/2026/01/critical-adonisjs-bodyparser-flaw-cvss.html){:target="_blank"}
