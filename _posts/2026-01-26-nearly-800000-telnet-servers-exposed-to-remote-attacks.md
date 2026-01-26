---
title: 'Nearly 800,000 Telnet servers exposed to remote attacks'
date: 2026-01-26
permalink: /posts/2026/01/26/nearly-800000-telnet-servers-exposed-to-remote-attacks/
tags:
- veille-cyber
- bleepingcomp
---
## Serveurs Telnet Vulnérables à l'Accès à Distance

Près de 800 000 adresses IP exposées sur Internet utilisent le service Telnet, et font l'objet d'attaques exploitant une faille critique de contournement d'authentification dans le serveur telnetd de GNU InetUtils. Cette vulnérabilité, identifiée sous le nom de CVE-2026-24061, affecte les versions 1.9.3 à 2.7 de GNU InetUtils, qui sont obsolètes. La faille permet à un attaquant d'envoyer des commandes spécialement conçues pour se connecter en tant que `root` sans nécessiter d'authentification, en manipulant la variable d'environnement `USER`.

Les attaques exploitant cette faille ont été détectées dès le 21 janvier, peu après sa correction dans la version 2.8 du logiciel. Les assaillants tentent d'obtenir un accès shell aux appareils compromis et ont également été observés déployant des malwares, bien que ces tentatives aient échoué sur certains systèmes. Les appareils concernés sont souvent des dispositifs IoT obsolètes où Telnet reste actif et exposé publiquement.

**Points Clés :**

*   Environ 800 000 instances Telnet sont exposées globalement.
*   La majorité de ces instances ne devraient pas être accessibles publiquement.
*   Telnet est fréquemment utilisé sur des appareils IoT hérités et intégrés.

**Vulnérabilités :**

*   **CVE-2026-24061 :** Contournement d'authentification critique dans le serveur telnetd de GNU InetUtils. Permet une connexion `root` sans authentification via la manipulation de la variable d'environnement `USER`.

**Recommandations :**

*   Mettre à jour le logiciel GNU InetUtils vers la version 2.8 ou une version ultérieure.
*   Si une mise à jour immédiate n'est pas possible, désactiver le service telnetd.
*   Bloquer le port TCP 23 sur tous les pare-feux pour empêcher l'accès externe.
*   Éviter l'exposition publique des serveurs Telnet, en particulier sur les appareils obsolètes.

---
[Source](https://www.bleepingcomputer.com/news/security/nearly-800-000-telnet-servers-exposed-to-remote-attacks/){:target="_blank"}
