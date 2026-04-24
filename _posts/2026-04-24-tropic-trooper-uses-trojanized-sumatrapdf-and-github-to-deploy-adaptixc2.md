---
title: 'Tropic Trooper Uses Trojanized SumatraPDF and GitHub to Deploy AdaptixC2'
date: 2026-04-24
permalink: /posts/2026/04/24/tropic-trooper-uses-trojanized-sumatrapdf-and-github-to-deploy-adaptixc2/
tags:
- veille-cyber
- hackernews
---
### Campagne de cyberespionnage du groupe Tropic Trooper via SumatraPDF

Le groupe APT « Tropic Trooper » (également connu sous les noms d'Earth Centaur ou Pirate Panda) mène actuellement une campagne ciblée visant des individus sinophones, notamment à Taïwan, au Japon et en Corée du Sud. Cette opération repose sur l'utilisation d'une version piégée du logiciel SumatraPDF pour compromettre les systèmes et établir un accès distant persistant.

**Points clés :**
* **Vecteur d'attaque :** Des archives ZIP contenant des documents leurres à thématique militaire incitent l'utilisateur à exécuter une version malveillante de SumatraPDF.
* **Méthodologie :** Le logiciel piégé déploie simultanément un document PDF légitime (pour le leurre) et un chargeur nommé « TOSHIS ». Ce dernier télécharge le framework d'exploitation « AdaptixC2 ».
* **Infrastructure :** Les attaquants utilisent GitHub comme plateforme de commande et de contrôle (C2) pour piloter l'agent AdaptixC2.
* **Escalade :** Sur les cibles jugées à haute valeur ajoutée, les attaquants installent Visual Studio Code et exploitent les tunnels VS Code pour obtenir un accès à distance persistant.
* **Historique :** Le groupe continue d'utiliser des outils connus comme EntryShell et Cobalt Strike, en plus de ses nouveaux frameworks de post-exploitation.

**Vulnérabilités :**
Aucune CVE spécifique n'est exploitée ; l'attaque repose sur l'exécution de code malveillant via des applications trojanisées et l'abus de fonctionnalités légitimes (VS Code Tunnels, GitHub).

**Recommandations :**
* **Vérification des logiciels :** Téléchargez uniquement les outils et lecteurs PDF depuis les sites officiels des éditeurs et vérifiez les signatures numériques des exécutables.
* **Sécurisation des accès :** Surveillez l'utilisation non autorisée des tunnels VS Code et restreignez les accès distants via des politiques de sécurité strictes.
* **Filtrage réseau :** Bloquez les communications suspectes vers GitHub ou d'autres plateformes de services cloud lorsqu'elles ne sont pas justifiées par une activité légitime de développement.
* **Sensibilisation :** Formez les utilisateurs à se méfier des archives contenant des documents « thématiques » envoyées par des sources non vérifiées.

---
[Source](https://thehackernews.com/2026/04/tropic-trooper-uses-trojanized.html){:target="_blank"}
