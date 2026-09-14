---
title: 'ISC Stormcast For Monday, September 14th, 2026 https://isc.sans.edu/podcastdetail/10092, (Mon, Sep 14th)'
date: 2026-09-14
permalink: /posts/2026/09/14/isc-stormcast-for-monday-september-14th-2026-httpsiscsansedupodcastdetail10092-mon-sep-14th/
tags:
- veille-cyber
- sans-isc
---
### L'évolution des CAPTCHA face aux attaquants automatisés

Cet article aborde la lutte permanente entre les systèmes de défi humain (CAPTCHA) et les outils d'automatisation. Bien que les CAPTCHA soient conçus pour distinguer les utilisateurs légitimes des robots, les attaquants utilisent désormais des services de résolution par IA ou via des humains (fermes à clics) pour contourner ces protections avec une efficacité croissante.

**Points clés :**
*   **Contournement par l'IA :** Les modèles de vision par ordinateur sont de plus en plus performants pour résoudre les puzzles visuels, rendant les anciennes méthodes (distorsion de texte, identification d'objets) obsolètes.
*   **Facteur humain :** L'externalisation de la résolution des défis vers des opérateurs humains à bas coût reste une technique très efficace pour les attaquants.
*   **Expérience utilisateur vs Sécurité :** La complexification des CAPTCHA pour contrer les bots dégrade significativement l'expérience des utilisateurs réels.

**Vulnérabilités :**
*   L'article souligne une vulnérabilité systémique dans la dépendance exclusive aux tests de type "Je suis un humain". Il ne cite pas de CVE spécifique, car il s'agit d'une faiblesse liée à l'exploitation de la logique métier (business logic abuse) et aux capacités de contournement des outils d'automatisation plutôt qu'à une faille logicielle isolée.

**Recommandations :**
*   **Approche multicouche :** Ne pas se reposer uniquement sur les CAPTCHA. Intégrer des outils d'analyse comportementale (empreintes de navigateur, analyse du mouvement de la souris, temps de réponse).
*   **Solutions "invisibles" :** Privilégier des mécanismes de détection en arrière-plan (comme reCAPTCHA v3 ou Turnstile) qui évaluent le score de risque sans interaction directe avec l'utilisateur.
*   **Limitation de débit (Rate Limiting) :** Mettre en place des restrictions strictes basées sur l'adresse IP et d'autres identifiants pour limiter l'impact des tentatives d'automatisation, même si elles passent le test CAPTCHA.
*   **Surveillance :** Analyser les logs pour identifier des schémas d'accès anormaux, souvent révélateurs de l'utilisation de services de résolution de captchas par des bots.

---
[Source](https://isc.sans.edu/diary/rss/33334){:target="_blank"}
