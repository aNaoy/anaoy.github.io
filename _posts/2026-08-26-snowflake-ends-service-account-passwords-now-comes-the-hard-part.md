---
title: 'Snowflake ends service-account passwords. Now comes the hard part'
date: 2026-08-26
permalink: /posts/2026/08/26/snowflake-ends-service-account-passwords-now-comes-the-hard-part/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des accès Snowflake : La fin des mots de passe pour les comptes de service

La plateforme Snowflake entame la phase finale de la suppression de l'authentification par mot de passe pour ses comptes de service (`LEGACY_SERVICE` vers `SERVICE`), en réponse à des campagnes massives de vol de données (notamment celle attribuée au groupe UNC5537). L'enjeu dépasse la simple mise à jour technique : il s'agit d'une dette d'identité accumulée au fil des années.

**Points clés :**
*   **Vulnérabilité identifiée :** L'usage massif d'identifiants valides mais compromis (volés parfois plusieurs années auparavant) couplé à une absence de double authentification (MFA) et de politiques réseau restrictives.
*   **Contexte de l'attaque :** Environ 80 % des comptes compromis lors des récentes campagnes de vol de données présentaient des traces d'exposition antérieure (ex: *infostealers*).
*   **Échéance :** La transition vers le type `SERVICE` (sans mot de passe) doit être finalisée entre août et octobre 2026 selon les instances.
*   **Défi majeur :** La difficulté ne réside pas dans la suppression du mot de passe, mais dans l'inventaire des dépendances et l'attribution de la propriété des comptes.

**Recommandations :**
1.  **Gouvernance active :** Identifier immédiatement les comptes utilisant encore des mots de passe via le schéma `ACCOUNT_USAGE` et leur affecter un propriétaire responsable (capable de gérer les incidents et le cycle de vie).
2.  **Choix des méthodes d'authentification :**
    *   **Priorité 1 :** Fédération d'identité (aucune clé stockée).
    *   **Priorité 2 :** OAuth externe.
    *   **Priorité 3 :** Paires de clés ou jetons programmatiques (uniquement avec des politiques réseau strictes et une rotation planifiée).
3.  **Nettoyage post-migration :** Considérer les anciens mots de passe comme définitivement compromis. Rechercher toute réutilisation de ces identifiants dans les pipelines CI/CD, les variables d'environnement ou les gestionnaires de secrets.
4.  **Prévention future :** Appliquer une rigueur identique aux nouveaux agents IA (`SERVICE_AGENT`) pour éviter de reproduire la dette d'identité actuelle.

---
[Source](https://www.bleepingcomputer.com/news/security/snowflake-ends-service-account-passwords-now-comes-the-hard-part/){:target="_blank"}
