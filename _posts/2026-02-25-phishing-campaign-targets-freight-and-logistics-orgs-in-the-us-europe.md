---
title: 'Phishing campaign targets freight and logistics orgs in the US, Europe'
date: 2026-02-25
permalink: /posts/2026/02/25/phishing-campaign-targets-freight-and-logistics-orgs-in-the-us-europe/
tags:
- veille-cyber
- bleepingcomp
---
**Vortex Diesel : Une campagne de phishing sophistiquée cible le secteur du fret**

Un groupe de cybercriminels identifié sous le nom de "Diesel Vortex" mène depuis septembre 2025 une campagne de phishing visant les entreprises de fret et de logistique aux États-Unis et en Europe. L'objectif est le vol de credentials, et plus de 1649 identifiants uniques ont déjà été dérobés à des plateformes et fournisseurs clés du secteur, tels que DAT Truckstop, TIMOCOM, Teleroute, Penske Logistics, Girteka et Electronic Funds Source (EFS).

Cette opération hautement organisée, qui ressemble à un centre d'appels et dispose d'un support commercial, utilise 52 domaines dédiés pour tromper les victimes. Les méthodes d'attaque incluent l'envoi d'emails de phishing utilisant des homoglyphes cyrilliques pour contourner les filtres, des appels vocaux frauduleux et l'infiltration de canaux Telegram fréquentés par le personnel du secteur. Les pages de phishing sont des copies fidèles des sites légitimes, conçues pour capturer des identifiants, des codes d'authentification à deux facteurs, des numéros d'identification (MC/DOT), et des informations de paiement. L'acteur semble être d'origine arménienne et connecté à des infrastructures russes.

Outre le vol de credentials, le groupe est suspecté de coordonner des activités de double courtage (double-brokering), consistant à usurper des identités de transporteurs pour détourner des chargements vers des points de retrait frauduleux afin de les voler.

Une action coordonnée impliquant plusieurs acteurs de la cybersécurité (GitLab, Cloudflare, Google Threat Intelligence, CrowdStrike, et Microsoft Threat Intelligence Center) a permis de perturber l'infrastructure de Diesel Vortex, incluant ses panneaux de contrôle et ses domaines de phishing.

**Points Clés :**

*   **Acteur malveillant :** "Diesel Vortex"
*   **Cible :** Organisations de fret et de logistique aux États-Unis et en Europe.
*   **Objectif :** Vol de credentials et fraude (double courtage, détournement de cargaisons).
*   **Méthodes :** Phishing par email (avec homoglyphes), phishing vocal, infiltration de canaux Telegram, création de pages de phishing imitant les plateformes légitimes.
*   **Plateformes ciblées :** DAT Truckstop, TIMOCOM, Teleroute, Penske Logistics, Girteka, EFS, ainsi que des plateformes de gestion de flotte, de cartes carburant et des bourses de fret.
*   **Origine suspectée :** Acteur arménien lié à des infrastructures russes.
*   **Impact :** Vol de 1649 credentials uniques, suspicion de détournement de cargaisons.

**Vulnérabilités :**

Bien que des CVEs spécifiques ne soient pas mentionnés dans l'article, les vulnérabilités exploitées sont liées à :

*   La confiance accordée aux emails et aux liens externes par les employés.
*   L'utilisation de plateformes critiques sans mesures de sécurité adéquates pour les employés de première ligne.
*   La possibilité pour les acteurs de créer des copies presque parfaites de sites légitimes.
*   L'exploitation de techniques d'ingénierie sociale.

**Recommandations :**

*   **Sensibilisation et formation des employés :** Renforcer la formation sur la détection des emails de phishing, la prudence face aux liens et aux demandes d'informations sensibles.
*   **Authentification multi-facteurs (MFA) :** Implémenter et forcer l'utilisation de l'authentification multi-facteurs sur toutes les plateformes critiques.
*   **Surveillance des accès et des activités :** Mettre en place une surveillance accrue des connexions aux comptes sensibles et des activités inhabituelles.
*   **Sécurité des plateformes en ligne :** S'assurer que les plateformes utilisées par le secteur du fret disposent de mesures de sécurité robustes et sont régulièrement mises à jour.
*   **Vérification des identités :** Mettre en place des procédures de vérification plus strictes pour confirmer l'identité des transporteurs et des demandes de chargement.
*   **Analyse des indicateurs de compromission (IoCs) :** Utiliser les IoCs partagés pour renforcer les défenses et détecter les activités malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/phishing-campaign-targets-freight-and-logistics-orgs-in-the-us-europe/){:target="_blank"}
