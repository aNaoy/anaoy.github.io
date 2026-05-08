---
title: 'Zara data breach exposed personal information of 197,000 people'
date: 2026-05-08
permalink: /posts/2026/05/08/zara-data-breach-exposed-personal-information-of-197000-people/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission des données clients chez Zara : 197 000 comptes exposés

Le groupe Inditex, maison mère de Zara, a confirmé une fuite de données impliquant les informations de 197 400 clients. L'incident ne provient pas des systèmes internes de l'enseigne, mais d'une intrusion chez un ancien prestataire technologique tiers. Le groupe cybercriminel « ShinyHunters » a revendiqué l'attaque, affirmant avoir accédé aux instances BigQuery du prestataire via des jetons d'authentification Anodot compromis.

**Points clés :**
*   **Volume :** 197 400 clients affectés.
*   **Nature des données volées :** Adresses e-mail uniques, références de produits (SKU), identifiants de commande, localisations géographiques et tickets de support.
*   **Données protégées :** Les identifiants de connexion, les informations de paiement, les noms, les adresses postales et les numéros de téléphone ne sont pas concernés.
*   **Responsabilité :** Le collectif ShinyHunters, spécialisé dans l'extorsion et le vol de données via des accès SaaS tiers.

**Vulnérabilités :**
*   **Usage de jetons d'authentification (tokens) :** L'utilisation malveillante de jetons Anodot a permis de contourner les protections standards pour accéder aux bases de données BigQuery.

**Recommandations :**
*   **Sécurisation des accès tiers :** Renforcer les protocoles de gestion des accès pour les prestataires externes (principes du moindre privilège et rotation fréquente des jetons d'authentification).
*   **Surveillance des comptes :** Les clients sont invités à rester vigilants face à d'éventuelles tentatives de phishing utilisant les données exposées (e-mails, références d'achats).
*   **Audit de sécurité :** Effectuer un audit rigoureux des flux de données partagés avec les partenaires technologiques et mettre en place des mécanismes d'authentification multifacteur (MFA) robustes sur tous les accès aux services cloud (SaaS/IaaS).

---
[Source](https://www.bleepingcomputer.com/news/security/zara-data-breach-exposed-personal-information-of-197-000-people/){:target="_blank"}
