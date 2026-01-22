---
title: 'Critical GNU InetUtils telnetd Flaw Lets Attackers Bypass Login and Gain Root Access'
date: 2026-01-22
permalink: /posts/2026/01/22/critical-gnu-inetutils-telnetd-flaw-lets-attackers-bypass-login-and-gain-root-access/
tags:
- veille-cyber
- hackernews
---
### Dépassement d'authentification critique dans GNU InetUtils telnetd

Une faille de sécurité majeure a été découverte dans le démon telnet de GNU InetUtils, baptisée **CVE-2026-24061**. Cette vulnérabilité, notée 9.8/10, affecte toutes les versions de GNU InetUtils de 1.9.3 à 2.7. Elle permet à des attaquants distants de contourner l'authentification et d'obtenir un accès "root" sur les systèmes ciblés.

**Points Clés :**

*   La vulnérabilité exploite la façon dont `telnetd` traite la variable d'environnement `USER` provenant du client.
*   En envoyant une valeur spécialement conçue ("-f root") pour `USER` via le paramètre `-a` ou `--login` de `telnet`, un attaquant peut déclencher le programme `login(1)` avec l'option `-f`, contournant ainsi le processus d'authentification normal.
*   Cette faille a été introduite dans le code source en mars 2015 et s'est retrouvée dans la version 1.9.3 sortie en mai 2015. Elle est restée méconnue pendant environ 11 ans.
*   Des tentatives d'exploitation de cette faille par 21 adresses IP distinctes provenant de diverses régions ont été observées récemment.

**Vulnérabilité :**

*   **CVE-2026-24061**

**Recommandations :**

*   Appliquer les derniers correctifs disponibles pour GNU InetUtils.
*   Restreindre l'accès réseau au port telnet aux clients de confiance.
*   Pour des solutions temporaires, désactiver le serveur `telnetd` ou configurer `InetUtils telnetd` pour utiliser un outil `login(1)` personnalisé qui n'accepte pas le paramètre `-f`.

---
[Source](https://thehackernews.com/2026/01/critical-gnu-inetutils-telnetd-flaw.html){:target="_blank"}
