---
title: 'HIBP Mega Update: Passkeys, k-Anonymity Searches, Massive Speed Enhancements and a Bulk Domain Verification API'
date: 2026-03-30
permalink: /posts/2026/03/30/hibp-mega-update-passkeys-k-anonymity-searches-massive-speed-enhancements-and-a-bulk-domain-verification-api/
tags:
- veille-cyber
- troyhunt
---
### Évolution majeure de Have I Been Pwned : Fonctionnalités, API et Performance

Have I Been Pwned (HIBP) annonce une mise à jour structurelle importante pour améliorer le support des organisations, l'automatisation et la protection de la vie privée.

**Points clés :**

*   **Refonte des plans d'abonnement :** Introduction de quatre nouveaux niveaux (Core, Pro, High RPM, Enterprise) pour mieux segmenter les besoins, notamment pour les MSP (Managed Service Providers) qui peuvent désormais surveiller les domaines de leurs clients.
*   **Automatisation de la vérification de domaines :** L'ajout de domaines peut désormais être automatisé via deux nouvelles API (DNS et E-mail), et la vérification d'un domaine racine valide désormais automatiquement tous ses sous-domaines pour les abonnés Pro.
*   **Confidentialité par k-anonymat :** L'API de recherche d'adresses e-mail comprometues propose désormais le *k-anonymat*. En envoyant uniquement les 6 premiers caractères du hash SHA-1 de l'adresse, l'utilisateur évite de transmettre des données identifiables à HIBP.
*   **Optimisation des performances :** Le système de limitation de débit (rate limit) a été assoupli pour permettre des rafales de requêtes, et la vérification des clés API a été déplacée en arrière-plan, réduisant le temps de réponse (Time to First Byte) de près de 40 %.
*   **Adoption des Passkeys :** L'authentification au tableau de bord HIBP est désormais possible via Passkeys, simplifiant la connexion sans compromettre la sécurité.
*   **Modifications tarifaires :** À partir d'août, une limite sur le nombre de domaines surveillés sera instaurée pour rationaliser les coûts SQL, et les tarifs seront harmonisés.

**Vulnérabilités et sécurité :**
*   Aucune CVE spécifique n'est mentionnée dans l'article.
*   L'article souligne l'importance d'utiliser le *k-anonymat* pour minimiser l'exposition des données personnelles (PII) lors des recherches.

**Recommandations :**

*   **Pour les entreprises :** Migrer vers les nouvelles API pour automatiser la gestion des domaines si vous gérez un large portefeuille ou si vous êtes un prestataire (MSP).
*   **Pour tous les utilisateurs :** Activer les *Passkeys* sur le tableau de bord HIBP pour une connexion plus rapide et sécurisée.
*   **Pour les développeurs :** Adopter l'approche par *k-anonymat* pour toute intégration future afin de renforcer la protection de la vie privée des utilisateurs finaux lors des requêtes d'exposition.
*   **Planification :** Les abonnés actuels doivent prendre connaissance des changements impactant leurs plans avant la mise en application prévue à partir d'août.

---
[Source](https://www.troyhunt.com/passkeys-k-anonymity-searches-massive-speed-enhancements-bulk-domain-verification-api/){:target="_blank"}
