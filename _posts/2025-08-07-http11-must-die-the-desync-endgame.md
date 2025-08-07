---
title: 'HTTP/1.1 must die: the desync endgame'
date: 2025-08-07
permalink: /posts/2025/08/07/http11-must-die-the-desync-endgame/
tags:
- veille-cyber
- zerodaysfans
---
### La fin de HTTP/1.1 : Le dernier acte de la désynchronisation

Le protocole HTTP/1.1 présente une faille de sécurité fondamentale qui expose des millions de sites web à des prises de contrôle malveillantes. Malgré plusieurs années de tentatives d'atténuation, le problème persiste. De nouvelles classes d'attaques de désynchronisation HTTP ont été découvertes, permettant des compromissions massives d'informations d'identification utilisateur. Ces techniques ont été exploitées pour découvrir des vulnérabilités critiques dans des infrastructures majeures telles qu'Akamai, Cloudflare et Netlify, affectant des dizaines de millions de sites web.

Un nouvel outil open-source a été développé pour faciliter la détection systématique des divergences entre les analyseurs de requêtes et des points faibles spécifiques aux cibles. L'utilisation combinée de ces techniques et de cet outil a permis de générer plus de 200 000 dollars en récompenses de bug bounty en deux semaines.

L'auteur soutient que la désynchronisation des requêtes HTTP doit être reconnue comme un défaut intrinsèque du protocole. Les solutions individuelles aux problèmes d'implémentation se sont avérées insuffisantes, laissant les sites web vulnérables à de futures variantes. Ces problèmes découlent d'une faille fatale dans HTTP/1.1, où des erreurs d'implémentation mineures peuvent entraîner des conséquences de sécurité graves. Le passage à HTTP/2 et aux versions ultérieures résout cette menace, et l'abandon de HTTP/1.1 est présenté comme la voie vers un web plus sécurisé.

**Points Clés :**

*   **Failles Fondamentales de HTTP/1.1 :** Le protocole souffre d'une mauvaise gestion des délimitations de requêtes et de multiples méthodes pour spécifier leur longueur, créant une ambiguïté exploitable.
*   **Atténuations Illusoires :** Les mesures de sécurité actuelles, comme la simplification des analyseurs ou la rétrogradation de HTTP/2 vers HTTP/1.1, masquent le problème sans le résoudre.
*   **Complexité Cachée :** Contrairement à la perception courante, la gestion de HTTP/1.1 devient complexe lorsqu'il est proxyfié, menant à des "pièges" dans la spécification et à des interactions imprévues.
*   **Nouvelles Techniques d'Attaque :** Des méthodes avancées comme les attaques 0.CL (basées sur une Content-Length vide) et celles exploitant l'en-tête `Expect` permettent de contourner les défenses existantes.
*   **Impact Massif :** Des vulnérabilités ont affecté des millions de sites web, démontrant la portée systémique de la faiblesse de HTTP/1.1.

**Vulnérabilités (avec CVE si possible) :**

*   Diverses vulnérabilités de désynchronisation de requêtes (Request Smuggling) exploitant des divergences entre analyseurs (ex: CL.TE, TE.CL, H2.0, 0.CL, TE.0, TE.TE).
*   Des vulnérabilités spécifiques ont été identifiées chez Akamai, Cloudflare et Netlify.
*   CVE-2025-32094 : Une vulnérabilité CL.0 via un en-tête `Expect` obfusqué sur Akamai CDN.

**Recommandations :**

*   **Adopter HTTP/2 :** Migrer vers HTTP/2 pour les connexions en amont des proxys afin de bénéficier d'une meilleure gestion des requêtes et de réduire considérablement le risque de désynchronisation.
*   **Activer le Support HTTP/2 en Amont :** S'assurer que les proxys et les équilibreurs de charge utilisent HTTP/2 pour communiquer avec les serveurs d'origine.
*   **Pour ceux qui sont bloqués sur HTTP/1.1 :**
    *   Activer toutes les options de normalisation et de validation sur les serveurs front-end et back-end.
    *   Privilégier des serveurs web courants comme Apache et Nginx.
    *   Effectuer des scans réguliers avec des outils comme "HTTP Request Smuggler".
    *   Envisager de désactiver la réutilisation des connexions en amont (avec un impact potentiel sur les performances).
    *   Rejeter les requêtes ayant un corps lorsqu'il n'est pas nécessaire (ex: pour les méthodes GET/HEAD/OPTIONS).
*   **Sensibilisation :** Informer sur la dangerosité de HTTP/1.1 et partager les découvertes pour encourager la migration.

---
[Source](https://portswigger.net/research/http1-must-die){:target="_blank"}
