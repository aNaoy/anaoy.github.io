---
title: 'Video service Vimeo confirms Anodot breach exposed user data'
date: 2026-04-29
permalink: /posts/2026/04/29/video-service-vimeo-confirms-anodot-breach-exposed-user-data/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez Vimeo via le fournisseur tiers Anodot

La plateforme vidéo Vimeo a subi un accès non autorisé à certaines de ses données suite à une compromission chez son prestataire de services, Anodot. Le groupe d'extorsion "ShinyHunters" a revendiqué l'attaque, menaçant de publier les données volées faute de paiement d'une rançon.

**Points clés :**
*   **Nature de l'incident :** Utilisation de jetons d'authentification dérobés chez Anodot pour accéder aux environnements cloud (Snowflake et BigQuery) de Vimeo.
*   **Données exposées :** Adresses e-mail, données techniques, titres de vidéos et métadonnées. 
*   **Données sécurisées :** Vimeo confirme que les vidéos elles-mêmes, les mots de passe et les informations de paiement n'ont pas été compromis.
*   **Impact opérationnel :** Les activités de Vimeo restent inchangées et opérationnelles.
*   **Auteurs :** Le groupe de cybercriminels ShinyHunters, connu pour cibler également d'autres organisations via des vecteurs similaires.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, l'incident résultant du vol de jetons d'authentification et d'une compromission de la chaîne d'approvisionnement (*supply chain attack*) via un service tiers (Anodot).

**Recommandations :**
*   **Isolement :** Vimeo a immédiatement révoqué tous les accès et identifiants liés au service Anodot.
*   **Remédiation :** Désactivation complète de l'intégration avec le système compromis.
*   **Investigation :** Lancement d'une enquête approfondie avec des experts en cybersécurité et signalement aux autorités judiciaires.
*   **Gestion des accès tiers :** Pour toute organisation, il est conseillé d'auditer régulièrement les privilèges accordés aux fournisseurs tiers et de renforcer la sécurité des accès via jetons (API tokens).

---
[Source](https://www.bleepingcomputer.com/news/security/video-service-vimeo-confirms-anodot-breach-exposed-user-data/){:target="_blank"}
