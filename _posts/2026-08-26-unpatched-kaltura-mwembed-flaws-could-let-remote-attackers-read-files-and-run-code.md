---
title: 'Unpatched Kaltura mwEmbed Flaws Could Let Remote Attackers Read Files and Run Code'
date: 2026-08-26
permalink: /posts/2026/08/26/unpatched-kaltura-mwembed-flaws-could-let-remote-attackers-read-files-and-run-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans la bibliothèque Kaltura mwEmbed

Le CERT/CC a révélé l'existence de deux vulnérabilités critiques non corrigées dans la bibliothèque de lecture vidéo HTML5 de Kaltura (`mwEmbed`). Ces failles permettent à un attaquant non authentifié d'exécuter du code arbitraire et de lire des fichiers sensibles sur les serveurs affectés. Le problème racine réside dans une désérialisation non sécurisée au sein du point de terminaison `mwEmbedLoader.php`, exacerbée par l'absence de réponse de l'éditeur malgré plusieurs tentatives de contact.

**Points clés :**
*   **Accessibilité :** Les vulnérabilités ne nécessitent aucune authentification. Elles touchent les installations individuelles ainsi que l'infrastructure CDN partagée de Kaltura.
*   **Gravité :** Les failles permettent la lecture de fichiers locaux (notamment des fichiers de configuration contenant des mots de passe en clair) et l'exécution de code à distance (RCE).
*   **Absence de correctif :** Aucun patch n'est disponible à ce jour. L'éditeur reste injoignable par les autorités de coordination.

**Vulnérabilités identifiées :**
*   **CVE-2026-19913 (Lecture arbitraire de fichiers) :** Exploitation du paramètre `ServiceUrl`. En manipulant ce paramètre avec un schéma `file://`, l'attaquant peut forcer le serveur à lire et renvoyer le contenu de fichiers locaux.
*   **CVE-2026-19912 (Exécution de code à distance - RCE) :** Exploitation du paramètre `uiconf_id`. Couplé à une désérialisation malveillante, ce paramètre permet d'écrire des fichiers PHP dans des répertoires accessibles par le serveur web via des séquences de traversée de répertoire (`../`).

**Recommandations pour les administrateurs :**
*   **Restriction d'accès :** Bloquer ou supprimer l'accès au point de terminaison `mwEmbedLoader.php` via un WAF ou un proxy inverse si l'utilisation de `mwEmbed` n'est pas strictement nécessaire.
*   **Filtrage (Allow-list) :** Restreindre strictement le paramètre `ServiceUrl` pour n'autoriser que les hôtes API légitimes et rejeter les schémas autres que HTTP(S).
*   **Sanitisation :** Rejeter toute valeur de `uiconf_id` contenant des caractères de séparation de répertoire ou des séquences de traversée (`../`).
*   **Durcissement :** Désactiver l'exécution de scripts PHP dans les répertoires de cache et restreindre les accès réseau sortants depuis le serveur d'application.
*   **Rotation des secrets :** En cas d'exposition, renouveler immédiatement toutes les informations contenues dans `local.ini` (mots de passe de base de données, clés API, identifiants administrateur).

---
[Source](https://thehackernews.com/2026/08/unpatched-kaltura-mwembed-flaws-could.html){:target="_blank"}
