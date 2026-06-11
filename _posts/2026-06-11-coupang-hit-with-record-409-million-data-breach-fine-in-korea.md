---
title: 'Coupang hit with record $409 million data breach fine in Korea'
date: 2026-06-11
permalink: /posts/2026/06/11/coupang-hit-with-record-409-million-data-breach-fine-in-korea/
tags:
- veille-cyber
- bleepingcomp
---
### Sanction record pour Coupang suite à une fuite massive de données

Le géant de l'e-commerce Coupang a écopé d'une amende historique de 409 millions de dollars de la part de la Commission de protection des informations personnelles (PIPC) de Corée du Sud, suite à une violation de données ayant compromis les informations de plus de 37 millions de clients.

**Points clés :**
*   **Ampleur du sinistre :** 37,55 millions de personnes touchées. La faille, survenue en juin, n'a été découverte qu'en novembre.
*   **Origine de l'incident :** L'intrusion a été attribuée à un ancien employé du département IT (2022-2024) ayant conservé des accès aux systèmes.
*   **Contexte aggravant :** L'enquête a révélé une obstruction de la part de l'entreprise, une ingérence dans l'indépendance du responsable de la protection des données et des manquements aux obligations de notification de fuite.
*   **Indemnisation :** Coupang a prévu de verser environ 1,17 milliard de dollars en compensations aux victimes à partir de 2026.

**Vulnérabilités identifiées :**
*   **Gestion des accès :** Défaut critique dans le contrôle des accès et la gestion des clés d'authentification (aucune CVE spécifique n'a été assignée, le problème relevant de négligences opérationnelles internes).
*   **Gouvernance des données :** Collecte et traitement illégaux de données sensibles, ainsi qu'un non-respect des protocoles de destruction des informations.

**Recommandations de sécurité :**
*   **Gestion du cycle de vie des accès :** Révoquer immédiatement tous les accès aux systèmes lors du départ d'un collaborateur (offboarding strict).
*   **Sécurisation des clés :** Centraliser et sécuriser la gestion des clés d'authentification par des systèmes de gestion des secrets (type Vault).
*   **Contrôles d'accès rigoureux :** Appliquer le principe du moindre privilège et segmenter les accès aux données sensibles pour limiter l'exposition en cas de compromission d'un compte interne.
*   **Conformité et transparence :** Renforcer l'indépendance des services de protection des données et garantir des procédures de notification d'incident conformes aux exigences réglementaires.

---
[Source](https://www.bleepingcomputer.com/news/security/south-korea-hits-coupang-with-record-409-million-fine-over-data-breach/){:target="_blank"}
