---
title: 'HTTP/1.1 must die: the desync endgame'
date: 2025-08-07
permalink: /posts/2025/08/07/http11-must-die-the-desync-endgame/
tags:
- veille-cyber
- zerodaysfans
---
### La Fin Inéluctable du Protocole HTTP/1.1 : Les Attaques par Désynchronisation

Le protocole HTTP/1.1 présente une vulnérabilité fondamentale dans la manière dont il traite les limites entre les requêtes. Cette faille, exploitée via des attaques de désynchronisation de requêtes (request smuggling), permet à des attaquants de détourner des millions de sites web, y compris des infrastructures critiques comme celles d'Akamai, Cloudflare et Netlify. Malgré des tentatives d'atténuation au cours des six dernières années, le problème persiste, car les correctifs ciblent les symptômes plutôt que la cause profonde. Les nouvelles classes d'attaques présentées, notamment celles exploitant l'en-tête `Expect` et les vulnérabilités de type 0.CL, ont révélé des failles dans des systèmes apparemment sécurisés, démontrant que même des versions obsolètes de protocoles peuvent causer des compromissions massives.

L'adoption généralisée d'HTTP/2 en amont (entre les serveurs) est présentée comme la seule solution durable. Ce protocole binaire élimine la plupart des ambiguïtés inhérentes à HTTP/1.1, rendant les attaques par désynchronisation beaucoup plus difficiles à réaliser.

**Points Clés :**

*   **Fragilité de HTTP/1.1 :** La concaténation des requêtes sur des sockets TCP sans délimiteurs clairs et les multiples méthodes de spécification de longueur créent des ambiguïtés exploitables.
*   **Attaques par Désynchronisation :** Les attaquants peuvent manipuler la manière dont les requêtes sont interprétées par différents composants d'une chaîne de serveurs (par exemple, proxy et serveur d'origine), leur permettant d'insérer des données malveillantes dans les requêtes des utilisateurs légitimes.
*   **Complexité des Mitigations :** Les tentatives de correction par le resserrement des analyseurs ou l'utilisation d'HTTP/2 côté client ne suffisent pas si la communication en amont reste en HTTP/1.1, surtout lorsque les proxys convertissent les requêtes HTTP/2 en HTTP/1.1.
*   **Impact Massif :** Des vulnérabilités découvertes ont potentiellement exposé des dizaines de millions de sites web, incluant des infrastructures majeures comme Akamai et Cloudflare, avec des exemples de détournement de sites web touchant des millions d'utilisateurs.
*   **Nouvelles Techniques :** L'article détaille de nouvelles classes d'attaques, notamment :
    *   **0.CL Desync :** Exploite l'absence d'en-tête `Content-Length` pour créer une désynchronisation, nécessitant un "gadget" de réponse anticipée pour être exploitable.
    *   **Expect-based Desync :** L'utilisation de l'en-tête `Expect`, même avec des formats standard ou légèrement obfusqués, peut révéler des désynchronisations, permettant par exemple des attaques de type 0.CL ou CL.0.
*   **Outil de Détection :** Un nouvel outil open-source, "HTTP Request Smuggler v3.0", est introduit pour détecter systématiquement les divergences d'analyseurs.
*   **Importance d'HTTP/2 :** La transition vers HTTP/2 en amont est fortement recommandée pour éliminer ce vecteur de menace.

**Vulnérabilités et CVEs :**

*   Des vulnérabilités critiques ont été découvertes et corrigées chez **Akamai**, **Cloudflare** et **Netlify**, exposant des millions de sites web. L'une d'elles a été attribuée le **CVE-2025-32094**.
*   Des failles ont été identifiées sur des systèmes utilisant **IIS derrière AWS Application Load Balancer (ALB)**, où AWS a choisi de ne pas patcher pour des raisons de compatibilité avec les clients HTTP/1.1 obsolètes.
*   Des problèmes ont été relevés avec des implémentations de l'en-tête `Expect` sur diverses plateformes, y compris **T-Mobile**, **GitLab** et **Akamai CDN**.

**Recommandations :**

*   **Migration vers HTTP/2 :** Passer à HTTP/2 pour les connexions en amont (entre le front-end et le serveur d'origine).
*   **Activation d'HTTP/2 sur les Proxies :** Les fournisseurs comme HAProxy, F5 Big-IP, Google Cloud, Imperva, Apache et Cloudflare permettent cette configuration. Les fournisseurs comme Nginx, Akamai, CloudFront et Fastly ne le supportent pas encore nativement en amont.
*   **Pour les systèmes restant sur HTTP/1.1 :**
    *   Activer toutes les options de normalisation et de validation sur les serveurs frontaux et d'origine.
    *   Privilégier les serveurs web réputés comme Apache et Nginx.
    *   Effectuer des analyses régulières avec des outils comme "HTTP Request Smuggler".
    *   Désactiver la réutilisation des connexions en amont si possible (peut impacter les performances).
    *   Rejeter les requêtes avec un corps pour les méthodes qui ne l'exigent pas (GET, HEAD, OPTIONS).
    *   Se méfier des affirmations selon lesquelles les WAFs peuvent efficacement contrer les désynchronisations autant qu'HTTP/2.
*   **Sensibilisation :** Partager les connaissances sur les dangers de HTTP/1.1 et encourager l'adoption de HTTP/2. Utiliser et contribuer à des outils comme "HTTP Request Smuggler".

---
[Source](https://portswigger.net/research/http1-must-die){:target="_blank"}
