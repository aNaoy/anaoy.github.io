---
title: 'CISA shares advice on isolating vital systems during cyberattacks'
date: 2026-07-28
permalink: /posts/2026/07/28/cisa-shares-advice-on-isolating-vital-systems-during-cyberattacks/
tags:
- veille-cyber
- bleepingcomp
---
### Stratégie d'isolement des infrastructures critiques face aux cybermenaces

Face à l'intensification des attaques ciblant les secteurs vitaux (énergie, eau, télécommunications), la CISA, le FBI et leurs partenaires internationaux ont publié le guide « CI Fortify ». Ce document préconise une planification rigoureuse pour isoler les systèmes de technologie opérationnelle (OT) en cas d'intrusion, afin d'empêcher les mouvements latéraux et de maintenir la continuité des services essentiels.

**Points clés :**
*   **Anticipation :** L'isolement ne doit pas être improvisé pendant une crise, mais testé et documenté à l'avance.
*   **Hiérarchisation :** Identifier les systèmes minimaux requis pour délivrer les services critiques.
*   **Types d'isolement :**
    *   *Physique :* Déconnexion totale (protection maximale).
    *   *Graduel :* Restriction progressive des accès (ex: couper les accès distants avant de couper le réseau d'entreprise).
    *   *Diodes de données :* Transfert unidirectionnel pour limiter l'entrée de trafic malveillant.
*   **Indépendance :** Conservation de copies hors ligne ou imprimées des plans d'urgence pour garantir l'accès même en cas de panne du réseau.
*   **Risques de l'isolement :** Difficulté de déploiement des mises à jour de sécurité et nécessité d'une maintenance manuelle accrue.

**Vulnérabilités mentionnées :**
Bien que l'article ne cite pas de CVE spécifiques, il souligne l'exploitation récurrente de **vulnérabilités connues dans les périphériques réseau (routeurs)** — notamment ceux utilisés par des groupes comme *Salt Typhoon* pour s'infiltrer — ainsi que l'utilisation de systèmes OT non sécurisés.

**Recommandations :**
*   **Cartographie :** Documenter précisément toutes les connexions entre les systèmes OT, le réseau d'entreprise, les accès distants et les prestataires.
*   **Points d'isolement :** Définir des zones de coupure prédéterminées pour contenir les menaces.
*   **Tests complets :** Tester régulièrement l'isolement global des systèmes pour identifier les dépendances cachées (infrastructures partagées).
*   **Supervision post-isolement :** Continuer à surveiller le trafic et les tables de routage après la déconnexion pour s'assurer qu'aucune connexion non autorisée ne se rétablit.
*   **Planification opérationnelle :** Préparer des processus manuels pour assurer le fonctionnement, la surveillance et la mise à jour des systèmes isolés.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-shares-advice-on-isolating-vital-systems-during-cyberattacks/){:target="_blank"}
