---
title: '[Webinar] Eliminate Ghost Identities Before They Expose Your Enterprise Data'
date: 2026-04-18
permalink: /posts/2026/04/18/webinar-eliminate-ghost-identities-before-they-expose-your-enterprise-data/
tags:
- veille-cyber
- hackernews
---
### Sécurisation des identités non-humaines : le risque des « comptes fantômes »

En 2024, 68 % des violations dans le cloud ont été causées par des identités non-humaines compromises (comptes de service, clés API, jetons OAuth, agents IA), plutôt que par des méthodes traditionnelles comme le phishing. La prolifération incontrôlée de ces identifiants, souvent hérités de projets terminés ou de départs de collaborateurs, crée des failles majeures : un seul jeton détourné peut offrir un accès administrateur et permettre une compromission persistante (durée moyenne d'intrusion supérieure à 200 jours).

**Points clés :**
*   **Déséquilibre :** Il existe en moyenne 40 à 50 identifiants automatisés pour chaque employé humain.
*   **Inadaptation des outils :** Les solutions de gestion des identités et des accès (IAM) classiques sont conçues pour les humains et peinent à superviser efficacement le cycle de vie des machines.
*   **Risque latéral :** La surprivilégisation des comptes de service facilite les mouvements latéraux des attaquants au sein du réseau.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car il se concentre sur une vulnérabilité systémique liée à une mauvaise configuration et à une absence de gestion du cycle de vie des identifiants (gestion des privilèges orphelins).

**Recommandations :**
*   **Audit exhaustif :** Réaliser une découverte complète de toutes les identités non-humaines présentes dans l'environnement.
*   **Principe du moindre privilège :** Réévaluer et ajuster les droits des comptes de service et des intégrations IA pour limiter les accès au strict nécessaire.
*   **Automatisation du cycle de vie :** Mettre en place des politiques de révocation automatique pour les identifiants obsolètes ou inutilisés.
*   **Mise en place de checklists :** Établir des procédures de nettoyage régulières pour éviter l'accumulation de "comptes fantômes".

---
[Source](https://thehackernews.com/2026/04/webinar-find-and-eliminate-orphaned-non.html){:target="_blank"}
