---
title: 'French hospital fined €500,000 after breach exposes data of 727,000'
date: 2026-09-04
permalink: /posts/2026/09/04/french-hospital-fined-500000-after-breach-exposes-data-of-727000/
tags:
- veille-cyber
- bleepingcomp
---
### Sanction financière contre l'Hôpital privé de la Loire pour faille de sécurité

La CNIL a infligé une amende de 500 000 € à l'Hôpital privé de la Loire (HPL) suite à une cyberattaque survenue à l'été 2025. Cette intrusion a entraîné l'exfiltration des données personnelles de 727 000 personnes, incluant des patients et des tiers de confiance. L'attaquant, un individu se faisant appeler « Marak », a compromis le compte d'un médecin pour infiltrer l'ensemble du système d'information de l'établissement.

**Points clés :**
*   **Vol de données :** 524 867 dossiers patients et 202 246 contacts de tiers de confiance ont été compromis.
*   **Vecteur d'attaque :** Compromission initiale d'un compte utilisateur (médecin libéral), permettant un mouvement latéral et un accès total aux données hospitalières.
*   **Absence de détection :** Le manque de surveillance en temps réel a permis au pirate d'exfiltrer les données sur plusieurs jours sans être alerté.

**Vulnérabilités identifiées :**
*   **Absence de MFA :** Accès au système autorisé sans authentification multifacteur.
*   **Accès à distance non sécurisé :** Utilisation possible du système sans VPN.
*   **Gestion des accès défaillante :** Cloisonnement insuffisant permettant à un compte unique d'accéder à l'intégralité de la base de données.
*   **Défaut de notification :** Manquement à l'obligation d'informer les tiers de confiance dont les données ont été dérobées.

**Recommandations :**
*   **Renforcement de l'authentification :** Implémentation systématique de l'authentification multifacteur (MFA) pour tous les accès distants et externes.
*   **Sécurisation des accès :** Systématiser l'usage de VPN pour les connexions des professionnels de santé externes.
*   **Monitoring et logs :** Déployer des outils de surveillance et d'alerte en temps réel pour détecter les comportements anormaux ou les exfiltrations massives de données.
*   **Principe du moindre privilège :** Restreindre strictement les droits d'accès des utilisateurs aux seules données nécessaires à leurs fonctions.
*   **Conformité RGPD :** Assurer la notification complète de toutes les personnes concernées en cas de violation de données (conformément aux articles 32 et 34 du RGPD).

---
[Source](https://www.bleepingcomputer.com/news/security/french-hospital-fined-500-000-after-breach-exposes-data-of-727-000/){:target="_blank"}
