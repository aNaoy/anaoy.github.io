---
title: 'AI-Assisted HTTP Terminator Finds Novel HTTP Desync Techniques and Apache Zero-Day'
date: 2026-08-07
permalink: /posts/2026/08/07/ai-assisted-http-terminator-finds-novel-http-desync-techniques-and-apache-zero-day/
tags:
- veille-cyber
- hackernews
---
### Découverte automatisée de vulnérabilités HTTP par IA

L'outil « HTTP Terminator », développé par James Kettle (PortSwigger), a automatisé la découverte de nouvelles techniques de désynchronisation HTTP. En analysant 138 documents RFC, l'IA a généré 30 000 vecteurs d'attaque, permettant d'identifier environ 700 cibles vulnérables, incluant des infrastructures bancaires et gouvernementales.

**Points clés :**
*   **Techniques innovantes :** Développement d'une méthode de « dangling-byte » rendant l'empoisonnement de la file d'attente de réponse (RQP) plus fiable en éliminant les conditions de concurrence (race conditions).
*   **Shared-Parser Confusion :** Une nouvelle catégorie d'attaque identifiée par l'IA, où les règles de traitement des réponses sont appliquées par erreur aux requêtes lors de la réutilisation de la logique d'analyse.
*   **Collaboration Homme-IA :** L'outil fonctionne de manière autonome pour la génération de vecteurs, mais nécessite une intervention humaine pour valider des concepts complexes comme le zero-day d'Apache.
*   **Open source :** L'outil est désormais disponible sur GitHub pour la recherche en sécurité.

**Vulnérabilités :**
*   **CVE-2026-63078 :** Vulnérabilité de désynchronisation HTTP découverte dans Apache Traffic Server (corrigée).

**Recommandations de sécurité :**
*   **Abandonner HTTP/1.1 :** Privilégier l'utilisation de protocoles modernes pour les flux amont (upstream).
*   **Renforcer les contrôles :** Si HTTP/1.1 est indispensable, mettre en place une liste blanche stricte des méthodes autorisées sur les deux couches (front-end/back-end).
*   **Restreindre les corps de requête :** Limiter rigoureusement les méthodes HTTP autorisées à transporter des corps de requête pour prévenir les injections.

---
[Source](https://thehackernews.com/2026/08/ai-assisted-http-terminator-finds-novel.html){:target="_blank"}
