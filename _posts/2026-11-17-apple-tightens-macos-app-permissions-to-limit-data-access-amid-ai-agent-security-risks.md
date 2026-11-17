---
title: 'Apple Tightens macOS App Permissions to Limit Data Access Amid AI Agent Security Risks'
date: 2026-11-17
permalink: /posts/2026/11/17/apple-tightens-macos-app-permissions-to-limit-data-access-amid-ai-agent-security-risks/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité macOS : Apple restreint l'accès aux données des applications

Apple renforce la sécurité et la confidentialité sur macOS (à partir de la version 27.3 beta 2) afin de limiter les risques associés aux agents d'intelligence artificielle. Ces mesures visent à offrir une meilleure transparence et un contrôle granulaire sur les autorisations accordées aux applications.

**Points clés :**
*   **Division des privilèges :** L'API « Device Control and Data Access » est scindée en deux paramètres distincts : *System & App Protection Override* et *Accessibility*.
*   **Transparence accrue :** Les utilisateurs sont désormais informés plus précisément de l'étendue des données accessibles lors de l'octroi de permissions complètes.
*   **Indicateurs de contrôle :** Une notification apparaît lorsqu'une application en contrôle une autre via *System & App Protection Override*.
*   **Configuration flexible :** Il est désormais possible de demander aux applications de solliciter l'autorisation à chaque accès nécessaire.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, mais ces changements répondent aux risques de sécurité accrus posés par les agents d'IA, capables d'exploiter des privilèges larges (comme le « Full Disk Access ») pour accéder à des données sensibles.

**Recommandations :**
*   **Pour les utilisateurs :** Restreindre l'accès au « Full Disk Access » à des dossiers spécifiques uniquement et privilégier l'option de demande systématique d'autorisation pour les applications sensibles.
*   **Pour les développeurs :** Mettre à jour les flux d'intégration (onboarding) des applications afin de gérer les scénarios où l'accès est limité à des dossiers ou des applications spécifiques. Prévoir l'utilisation d'autorisations spéciales (« entitlements ») pour maintenir les fonctionnalités existantes sur les nouvelles installations.

---
[Source](https://thehackernews.com/2026/11/apple-tightens-macos-app-permissions-to.html){:target="_blank"}
