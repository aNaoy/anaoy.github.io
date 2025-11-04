---
title: 'Critical React Native CLI Flaw Exposed Millions of Developers to Remote Attacks'
date: 2025-11-04
permalink: /posts/2025/11/04/critical-react-native-cli-flaw-exposed-millions-of-developers-to-remote-attacks/
tags:
- veille-cyber
- hackernews
---
### Exploitation de Commandes Arbitraires via React Native CLI

Une faille de sécurité critique affectant le package npm "@react-native-community/cli" permettait l'exécution de commandes système à distance sur les machines des développeurs. La vulnérabilité, identifiée sous le nom de CVE-2025-11953, présentait un score de sévérité critique (9.8/10). Les versions 4.8.0 à 20.0.0-alpha.2 du package "@react-native-community/cli-server-api" étaient concernées.

**Points Clés :**

*   **Nature de la vulnérabilité :** Permettait l'exécution de commandes arbitraires du système d'exploitation (OS) par des attaquants non authentifiés à distance.
*   **Cible :** Les machines exécutant le serveur de développement de "react-native-community/cli".
*   **Mécanisme d'exploitation :** Le serveur de développement Metro, utilisé par React Native, liait par défaut ses interfaces externes et exposait un point d'accès "/open-url". Ce dernier traitait des requêtes POST contenant des entrées utilisateur qui étaient passées à la fonction `open()` du package `open` (NPM), menant à l'exécution de commandes système.
*   **Impact :** Sur Windows, les attaquants pouvaient exécuter des commandes shell avec des arguments entièrement contrôlés. Sur Linux et macOS, l'exploitation permettait l'exécution de binaires arbitraires avec un contrôle limité des paramètres.
*   **Facilité d'exploitation :** La vulnérabilité était jugée dangereuse en raison de sa facilité d'exploitation, de l'absence de nécessité d'authentification et de sa large surface d'attaque.
*   **Portée :** Le package "@react-native-community/cli" enregistre entre 1,5 et 2 millions de téléchargements par semaine, soulignant l'ampleur du risque potentiel.

**Vulnérabilité :**

*   **CVE-2025-11953**

**Recommandations :**

*   Les développeurs utilisant React Native doivent mettre à jour le package "@react-native-community/cli" vers la version **20.0.0** ou une version ultérieure.
*   Il est crucial de maintenir une veille et une analyse de sécurité automatisées et complètes de la chaîne d'approvisionnement logicielle pour identifier et corriger les failles avant qu'elles n'impactent les organisations.

Il est important de noter que les développeurs utilisant des frameworks React Native qui ne s'appuient pas sur Metro comme serveur de développement ne sont pas affectés par cette faille.

---
[Source](https://thehackernews.com/2025/11/critical-react-native-cli-flaw-exposed.html){:target="_blank"}
