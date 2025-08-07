---
title: 'HTTP/1.1 must die: the desync endgame'
date: 2025-08-07
permalink: /posts/2025/08/07/http11-must-die-the-desync-endgame/
tags:
- veille-cyber
- zerodaysfans
---
## HTTP/1.1 : La Fin d'un Protocole Vulnérable

Le protocole HTTP/1.1, malgré sa présence généralisée, souffre d'une faille de conception fondamentale : la gestion floue des limites entre les requêtes. Cette faiblesse intrinsèque permet aux attaquants de créer des désynchronisations de requêtes (request smuggling), ouvrant la voie à des prises de contrôle de sites web, au vol d'informations d'identification et à d'autres attaques graves. Malgré des années de tentatives d'atténuation, le problème persiste, caché sous une illusion de sécurité.

### Points Clés

*   **Désynchronisation de Requêtes (Request Smuggling)** : Les différences dans la manière dont les serveurs frontaux et les serveurs back-end interprètent les longueurs des requêtes HTTP/1.1 créent une ambiguïté exploitable.
*   **Complexité Accrue par les Proxys et la Migration H2** : L'utilisation de proxys inverses et la rétrogradation des requêtes HTTP/2 vers HTTP/1.1 pour la communication interne compliquent la gestion des requêtes et introduisent de nouvelles vecteurs d'attaque.
*   **Attaques "0.CL" et "Expect"** : De nouvelles classes d'attaques basées sur la manipulation de l'en-tête `Content-Length` (0.CL) et de l'en-tête `Expect` ont été découvertes, permettant des compromissions étendues, y compris sur des infrastructures critiques.
*   **Atténuations Inefficaces** : Les correctifs appliqués aux implémentations individuelles ne résolvent pas la faille fondamentale du protocole, se contentant de rendre les méthodes d'exploitation classiques plus difficiles.

### Vulnérabilités Découvertes (Exemples)

*   **Cloudflare (H2.0 desync)** : Une désynchronisation interne à l'infrastructure de Cloudflare, exploitant une rétrogradation de HTTP/2 à HTTP/1.1, a exposé plus de 24 millions de sites web à des prises de contrôle.
*   **Akamai CDN (CL.0 desync via obfuscated Expect)** : Une vulnérabilité exploitant une désynchronisation CL.0 via un en-tête `Expect` obfusqué a permis de servir du contenu arbitraire sur `auth.lastpass.com`, et affectait potentiellement d'autres domaines majeurs comme `example.com`. Cette vulnérabilité a été identifiée sous la référence **CVE-2025-32094**.
*   **GitLab (0.CL desync via obfuscated Expect)** : Une désynchronisation 0.CL via un en-tête `Expect` légèrement obfusqué a été trouvée sur `h1.sec.gitlab.net`, permettant des attaques de "Response Queue Poisoning" sur les rapports de bug bounty.
*   **Netlify CDN (CL.0 RQP)** : Une vulnérabilité de "Response Queue Poisoning" a été découverte sur le CDN de Netlify, exposant des réponses de plusieurs sites hébergés sur la plateforme.
*   **T-Mobile (0.CL desync via vanilla Expect)** : Une désynchronisation 0.CL via un en-tête `Expect` standard a été exploitée sur un domaine de staging de T-Mobile.

D'autres vulnérabilités ont été identifiées sur des infrastructures comme Akamai, Cloudflare, Netlify, ainsi que sur des systèmes utilisant IIS derrière AWS ALB, mettant en évidence la généralisation du problème.

### Recommandations

*   **Migration vers HTTP/2 (ou supérieur)** : La seule solution à long terme est de passer à des protocoles plus modernes comme HTTP/2, qui éliminent la problématique de la désynchronisation grâce à leur nature binaire et à une gestion claire de la longueur des messages.
*   **Activer le HTTP/2 en amont (Upstream HTTP/2)** : Configurer les proxys et les équilibreurs de charge pour utiliser HTTP/2 pour la communication avec les serveurs back-end. Les fournisseurs comme Nginx, Akamai, et CloudFront doivent encore ajouter cette fonctionnalité.
*   **Pour ceux bloqués avec HTTP/1.1** :
    *   Activer toutes les options de normalisation et de validation sur les serveurs frontaux et back-end.
    *   Privilégier des serveurs web courants comme Apache ou Nginx.
    *   Effectuer des scans réguliers avec des outils dédiés comme "HTTP Request Smuggler".
    *   Désactiver la réutilisation des connexions en amont si possible (impact potentiel sur les performances).
    *   Rejeter les requêtes ayant un corps alors que la méthode ne le requiert pas (par ex. GET, HEAD).
    *   Être sceptique quant aux affirmations des fournisseurs de WAFs sur leur capacité à contrer efficacement les désynchronisations de requêtes par rapport à HTTP/2.
*   **Sensibilisation et Partage d'Informations** : Augmenter la prise de conscience sur les dangers de HTTP/1.1 et encourager le partage des découvertes et des méthodes d'exploitation pour accélérer la transition vers des protocoles plus sûrs.

---
[Source](https://portswigger.net/research/http1-must-die){:target="_blank"}
