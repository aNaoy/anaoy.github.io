---
title: 'UK govt. warns about ongoing Russian hacktivist group attacks'
date: 2026-01-19
permalink: /posts/2026/01/19/uk-govt-warns-about-ongoing-russian-hacktivist-group-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Alerte sur les cyberattaques russes : infrastructure critique et gouvernements locaux sous pression**

Les groupes de pirates informatiques pro-russes intensifient leurs attaques, principalement par des dénis de service distribués (DDoS), visant les infrastructures critiques et les organisations gouvernementales locales au Royaume-Uni. Ces attaques, bien que souvent rudimentaires, peuvent entraîner des perturbations majeures, des coûts importants et une perte de résilience opérationnelle pour les entités ciblées.

Le Centre National de Cybersécurité (NCSC) du Royaume-Uni a notamment pointé du doigt le groupe NoName057(16), actif depuis mars 2022 et moteur du projet DDoSia qui permet des attaques coordonnées par une communauté de volontaires. Malgré une opération internationale ayant perturbé le groupe à mi-juillet 2025, ses principaux opérateurs, présumés basés en Russie, ont permis son retour en activité. Le NCSC souligne que ces groupes sont motivés par des idéologies plutôt que par des gains financiers et représentent une menace croissante, s'étendant désormais aux environnements opérationnels (OT).

**Points Clés :**

*   **Nature des attaques :** Déni de service distribué (DDoS) visant à rendre les sites web et services indisponibles.
*   **Acteurs :** Groupes de hacktivistes pro-russes, notamment NoName057(16).
*   **Cibles :** Infrastructures critiques et organisations gouvernementales locales au Royaume-Uni, ainsi que des entités dans les pays de l'OTAN et européens s'opposant aux ambitions géopolitiques russes.
*   **Motivation :** Idéologique.
*   **Impact :** Perturbation des systèmes, coûts financiers, perte de temps, nécessité d'analyse et de récupération, menace sur la résilience opérationnelle, potentielle atteinte aux environnements OT.

**Vulnérabilités :**

*   Les attaques DDoS exploitent la saturation des ressources système, conduisant à une indisponibilité des services. Aucune vulnérabilité CVE spécifique n'est mentionnée dans l'article, car les attaques DDoS ciblent généralement la disponibilité plutôt que des failles logicielles précises.

**Recommandations (NCSC) :**

*   **Compréhension des services :** Identifier les points de potentielle exhaustion de ressources et les limites de responsabilité.
*   **Renforcement des défenses :** Mettre en place des protections en amont, incluant les mesures des fournisseurs d'accès internet (FAI), les services tiers de protection DDoS, les réseaux de diffusion de contenu (CDN) et les protections imposées par les fournisseurs. Envisager la redondance avec plusieurs fournisseurs.
*   **Conception pour la scalabilité :** Permettre une mise à l'échelle rapide grâce à l'auto-scalabilité cloud ou à la virtualisation avec une capacité excédentaire.
*   **Plans de réponse :** Définir et répéter des plans de réponse incluant une dégradation progressive des services (graceful degradation), l'adaptation aux tactiques changeantes des attaquants, le maintien de l'accès administrateur et des solutions de repli évolutives pour les services essentiels.
*   **Tests et surveillance continus :** Détecter les attaques précocement et valider l'efficacité des défenses.

---
[Source](https://www.bleepingcomputer.com/news/security/uk-govt-warns-about-ongoing-russian-hacktivist-group-attacks/){:target="_blank"}
