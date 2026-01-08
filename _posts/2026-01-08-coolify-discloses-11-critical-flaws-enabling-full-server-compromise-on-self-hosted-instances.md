---
title: 'Coolify Discloses 11 Critical Flaws Enabling Full Server Compromise on Self-Hosted Instances'
date: 2026-01-08
permalink: /posts/2026/01/08/coolify-discloses-11-critical-flaws-enabling-full-server-compromise-on-self-hosted-instances/
tags:
- veille-cyber
- hackernews
---
## Vulnérabilités Critiques Impactant la Plateforme d'Auto-hébergement Coolify

La plateforme d'auto-hébergement open-source Coolify est affectée par un ensemble de onze vulnérabilités critiques. Ces failles de sécurité, pour la plupart liées à l'injection de commandes, permettent à des attaquants d'obtenir l'exécution de code arbitraire, d'outrepasser l'authentification et, in fine, de compromettre entièrement les serveurs hébergés.

**Points Clés et Vulnérabilités :**

*   **Injection de Commandes :** Plusieurs vulnérabilités (listées ci-dessous avec leurs CVE respectives) permettent à des utilisateurs authentifiés, voire à des utilisateurs à faibles privilèges selon les cas, d'exécuter des commandes système arbitraires avec des privilèges élevés (y compris root). Ces failles sont présentes dans des fonctionnalités telles que la sauvegarde de bases de données, l'importation de bases de données, la gestion des scripts d'initialisation PostgreSQL, la configuration de proxy dynamique, le montage de répertoires de stockage de fichiers, et l'utilisation de `docker-compose.yaml`.
*   **Divulgation d'Informations Sensibles :** Une vulnérabilité permet à des utilisateurs à faibles privilèges de consulter la clé privée de l'utilisateur root, ouvrant la porte à une connexion non autorisée par SSH.
*   **Cross-Site Scripting (XSS) Stocké :** Une faille permet une attaque XSS stockée lors de la création de projets, qui s'exécute automatiquement dans le navigateur d'un administrateur lors de certaines actions.

**Liste des Vulnérabilités Identifiées :**

*   CVE-2025-66209 (CVSS 10.0) : Injection de commande dans la sauvegarde de base de données.
*   CVE-2025-66210 (CVSS 10.0) : Injection de commande dans l'importation de base de données.
*   CVE-2025-66211 (CVSS 10.0) : Injection de commande dans la gestion des scripts d'initialisation PostgreSQL.
*   CVE-2025-66212 (CVSS 10.0) : Injection de commande dans la configuration du proxy dynamique.
*   CVE-2025-66213 (CVSS 10.0) : Injection de commande dans le montage des répertoires de stockage de fichiers.
*   CVE-2025-64419 (CVSS 9.7) : Injection de commande via `docker-compose.yaml`.
*   CVE-2025-64420 (CVSS 10.0) : Divulgation de la clé privée root.
*   CVE-2025-64424 (CVSS 9.4) : Injection de commande dans les champs d'entrée git.
*   CVE-2025-59156 (CVSS 9.4) : Injection de commande système via des directives Docker Compose.
*   CVE-2025-59157 (CVSS 10.0) : Injection de commandes shell via le champ dépôt Git.
*   CVE-2025-59158 (CVSS 9.4) : Attaque XSS stockée lors de la création de projet.

**Versions Impactées et Recommandations :**

Les versions antérieures à celles spécifiées ci-dessous sont vulnérables. Il est fortement recommandé aux utilisateurs de mettre à jour leurs instances Coolify vers les versions corrigées dès que possible.

*   CVE-2025-66209, CVE-2025-66210, CVE-2025-66211 : versions inférieures ou égales à 4.0.0-beta.448 (corrigé à partir de 4.0.0-beta.451).
*   CVE-2025-66212, CVE-2025-66213 : versions inférieures ou égales à 4.0.0-beta.450 (corrigé à partir de 4.0.0-beta.451).
*   CVE-2025-64419 : versions antérieures à 4.0.0-beta.436 (corrigé à partir de 4.0.0-beta.445).
*   CVE-2025-64420, CVE-2025-64424 : versions inférieures ou égales à 4.0.0-beta.434 (statut de correction non clair).
*   CVE-2025-59156, CVE-2025-59157, CVE-2025-59158 : versions inférieures ou égales à 4.0.0-beta.420.6 (corrigé à partir de 4.0.0-beta.420.7).

Bien qu'aucune exploitation de ces failles n'ait été détectée pour le moment, la gravité des vulnérabilités impose une action immédiate pour sécuriser les installations.

---
[Source](https://thehackernews.com/2026/01/coolify-discloses-11-critical-flaws.html){:target="_blank"}
