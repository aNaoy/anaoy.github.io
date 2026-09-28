---
title: 'Misconfigured Supabase apps expose data in over 16,000 databases'
date: 2026-09-28
permalink: /posts/2026/09/28/misconfigured-supabase-apps-expose-data-in-over-16000-databases/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive via des bases de données Supabase mal configurées

Plus de 16 000 bases de données Supabase ont été identifiées comme étant exposées publiquement, permettant l'accès à des informations sensibles telles que des données personnelles (PII), des mots de passe en clair, des jetons d'authentification et, dans certains cas, des données de cartes bancaires. Cette vulnérabilité touche des secteurs variés (services gouvernementaux, plateformes de contenu, services de transport) et semble corrélée à une utilisation accrue d'outils de développement assistés par IA, où les utilisateurs omettent souvent de configurer correctement les paramètres de sécurité.

**Points clés :**
*   **Cause racine :** Une mauvaise configuration des politiques de sécurité au niveau des lignes (Row-Level Security - RLS) et une utilisation inappropriée des clés publiques.
*   **Facteur aggravant :** L'usage d'agents de codage IA qui facilite le déploiement rapide mais laisse les utilisateurs sans connaissance précise de la sécurisation réelle de leur base de données.
*   **Impact :** Exposition de millions d'enregistrements incluant des historiques de visite, des messages privés, des identifiants et des données biométriques ou financières.
*   **Vulnérabilités :** Il ne s'agit pas d'une faille logicielle (CVE), mais d'une erreur de configuration systémique par les développeurs.

**Recommandations :**
*   **Auditer les accès :** Vérifier immédiatement les politiques de sécurité (RLS) sur toutes les tables de la base de données.
*   **Documentation technique :** Consulter les guides officiels de Supabase sur la [sécurisation des API](https://supabase.com/docs/guides/api/securing-your-api) et utiliser les outils d'observabilité intégrés (Advisors) pour détecter les expositions accidentelles.
*   **Responsabilisation humaine :** Ne pas se reposer exclusivement sur le code généré par l'IA et valider manuellement les paramètres de contrôle d'accès après chaque déploiement.

---
[Source](https://www.bleepingcomputer.com/news/security/misconfigured-supabase-apps-expose-data-in-over-16-000-databases/){:target="_blank"}
