---
title: 'Highly Critical Drupal Core Flaw Exposes PostgreSQL Sites to RCE Attacks'
date: 2026-05-21
permalink: /posts/2026/05/21/highly-critical-drupal-core-flaw-exposes-postgresql-sites-to-rce-attacks/
tags:
- veille-cyber
- hackernews
---
### Faille critique dans Drupal Core : Risque d'exécution de code à distance

Une vulnérabilité critique affectant l'API d'abstraction de base de données de Drupal Core expose les sites utilisant PostgreSQL à des attaques par injection SQL.

**Points clés :**
*   **Vecteur d'attaque :** Des utilisateurs anonymes peuvent envoyer des requêtes spécialement conçues pour exploiter l'API.
*   **Impact :** Divulgation d'informations, élévation de privilèges et exécution de code à distance (RCE).
*   **Périmètre :** La faille concerne exclusivement les sites utilisant une base de données PostgreSQL. Drupal 7 n'est pas affecté.

**Vulnérabilité :**
*   **CVE-2026-9082 :** Score CVSS de 6,5/10.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquez les dernières versions de Drupal : 11.3.10, 11.2.12, 11.1.10, 10.6.9, 10.5.10 ou 10.4.10. Ces mises à jour incluent également des correctifs de sécurité pour les bibliothèques Symfony et Twig.
*   **Versions obsolètes :** Pour les versions en fin de vie (Drupal 8.9 et 9.5), des correctifs manuels sont disponibles "au mieux", bien que ces versions restent vulnérables à d'autres failles non corrigées. Il est fortement conseillé de migrer vers une version supportée.

---
[Source](https://thehackernews.com/2026/05/highly-critical-drupal-core-flaw.html){:target="_blank"}
