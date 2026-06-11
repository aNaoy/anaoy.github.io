---
title: 'GitHub announces npm security changes to tackle supply-chain attacks'
date: 2026-06-11
permalink: /posts/2026/06/11/github-announces-npm-security-changes-to-tackle-supply-chain-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement de la sécurité de la chaîne d'approvisionnement dans npm v12

GitHub a annoncé des modifications majeures pour la version 12 de npm, visant à neutraliser les attaques par chaîne d'approvisionnement exploitant l'automatisation de la commande `npm install`. Désormais, les comportements jusqu'ici privilégiés par défaut devront faire l'objet d'une approbation explicite.

**Points clés des changements :**
*   **Scripts d'installation :** Les scripts `preinstall`, `install`, `postinstall` (ainsi que les builds `node-gyp` et les scripts `prepare`) ne seront plus exécutés automatiquement.
*   **Dépendances Git :** La récupération de dépendances depuis des dépôts Git (directes ou transitives) sera bloquée par défaut pour prévenir l'exécution de code malveillant via des fichiers `.npmrc` détournés.
*   **Sources externes :** Les dépendances provenant d'URL distantes (ex: archives HTTPS) nécessiteront une autorisation explicite pour être résolues.

**Vulnérabilités adressées :**
Ces mesures visent à bloquer des vecteurs d'attaque récurrents, tels que :
*   L'exécution automatique de scripts malveillants lors de l'installation (utilisée par des campagnes comme *Shai-Hulud*).
*   Le détournement de paquets populaires (ex: *eslint-config-prettier*, *Picasso*) pour l'exfiltration de données.
*   L'abus de dépendances Git pour contourner les protections existantes.
*(Note : Aucune CVE spécifique n'est mentionnée dans l'article, ces changements agissant comme une mesure de protection structurelle contre des classes d'attaques.)*

**Recommandations :**
*   **Anticipation :** Mettre à jour vers **npm 11.16.0** ou une version supérieure dès maintenant. Cette version émettra des avertissements pour chaque action qui sera bloquée par la v12, permettant d'identifier les dépendances ou workflows nécessitant une configuration manuelle.
*   **Audit :** Examiner les avertissements générés lors de l'exécution de `npm install` pour cartographier les workflows légitimes devant faire l'objet d'une approbation explicite avant la migration vers la v12.

---
[Source](https://www.bleepingcomputer.com/news/security/github-announces-npm-security-changes-to-tackle-supply-chain-attacks/){:target="_blank"}
