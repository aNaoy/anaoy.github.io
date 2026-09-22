---
title: 'BigCommerce alerts merchants of data breach linked to Ribon apps'
date: 2026-09-22
permalink: /posts/2026/09/22/bigcommerce-alerts-merchants-of-data-breach-linked-to-ribon-apps/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de données chez BigCommerce via les applications Ribon

La plateforme e-commerce BigCommerce a alerté ses marchands suite à une compromission des identifiants des applications tierces « Ribon » et « Ribon 1.5 ». Les attaquants ont utilisé ces clés d'accès pour injecter des scripts malveillants et accéder aux bases de données clients de plusieurs boutiques en ligne entre le 13 et le 17 septembre.

**Points clés :**
*   **Nature de l'attaque :** Vol de clés d'API appartenant à l'éditeur tiers « Be A Part Of » (filiale de Fastr), permettant une intrusion dans les environnements marchands via des applications intégrées.
*   **Données exposées :** Noms complets, adresses électroniques, numéros de téléphone et adresses postales de livraison.
*   **Périmètre :** La plateforme BigCommerce elle-même n'a pas été compromise. Les mots de passe des comptes et les données de cartes bancaires sont stockés séparément et n'ont pas été affectés.
*   **Réaction :** BigCommerce a immédiatement désinstallé les applications incriminées des boutiques concernées et notifié les marchands impactés.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une compromission de clés d'accès tierces (gestion des accès et des permissions d'applications tierces).

**Recommandations :**
*   **Révision des privilèges :** Les marchands utilisant des plateformes SaaS doivent auditer régulièrement les permissions accordées aux applications tierces (principe du moindre privilège).
*   **Surveillance des intégrations :** Limiter l'installation d'applications tierces non essentielles et surveiller les accès accordés à des composants externes.
*   **Notification :** En cas de doute, les marchands concernés doivent suivre les procédures de conformité (comme le RGPD) et informer leurs clients de l'exposition potentielle de leurs données personnelles.

---
[Source](https://www.bleepingcomputer.com/news/security/bigcommerce-alerts-merchants-of-data-breach-linked-to-ribon-apps/){:target="_blank"}
