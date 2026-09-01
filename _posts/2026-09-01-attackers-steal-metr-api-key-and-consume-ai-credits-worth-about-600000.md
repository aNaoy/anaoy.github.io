---
title: 'Attackers Steal METR API Key and Consume AI Credits Worth About $600,000'
date: 2026-09-01
permalink: /posts/2026/09/01/attackers-steal-metr-api-key-and-consume-ai-credits-worth-about-600000/
tags:
- veille-cyber
- hackernews
---
### Vol de clés API et cyberattaques contre l'organisation METR

L'organisation de recherche en IA, METR, a subi deux incidents de sécurité majeurs en 2026, entraînant le vol d'une clé API et la consommation frauduleuse de crédits cloud estimés à 600 000 $.

**Points clés :**
*   **Incident de mars :** Une clé API a été compromise via une instance EC2 personnelle mal configurée. Les attaquants ont utilisé une vulnérabilité de type "fail-open" pour contourner l'authentification et accéder aux ressources.
*   **Incident de mai :** Une campagne systématique d'attaques a ciblé l'infrastructure publique de METR par du *credential stuffing*, du phishing et l'exploitation d'une vulnérabilité dans un outil de consultation de transcriptions.
*   **Impact financier :** La compromission a permis une consommation massive de jetons sur des modèles d'IA. Le montant total a été absorbé par le fournisseur de services, évitant une perte réelle pour l'organisation.

**Vulnérabilités identifiées :**
*   **Fail-open (OWASP) :** Configuration défaillante d'une application entraînant le contournement total de l'authentification.
*   **Exposition accidentelle d'endpoint :** Une vulnérabilité dans un composant de requête SQL permettait potentiellement d'accéder à des données de recherche non publiées.
*   **Configuration de base de données :** Inclusion accidentelle de données sensibles dans un accès supposé public.

**Recommandations :**
*   **Strict contrôle des accès :** Interdire le stockage de clés API ou de données confidentielles sur des infrastructures ou appareils personnels/non gérés.
*   **Gestion des coûts :** Mettre en place des plafonds de dépenses (spend caps) et des alertes automatiques sur toutes les clés API pour détecter les pics d'utilisation anormaux.
*   **Monitoring renforcé :** Améliorer la surveillance des accès aux endpoints publics pour détecter les sondages automatisés et les tentatives de force brute.
*   **Sécurisation du cycle de vie des données :** Audit régulier des endpoints exposés et cloisonnement strict entre les jeux de données publics et les données de recherche sensibles.

---
[Source](https://thehackernews.com/2026/09/attackers-steal-metr-api-key-and.html){:target="_blank"}
