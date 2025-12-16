---
title: 'Amazon Exposes Years-Long GRU Cyber Campaign Targeting Energy and Cloud Infrastructure'
date: 2025-12-16
permalink: /posts/2025/12/16/amazon-exposes-years-long-gru-cyber-campaign-targeting-energy-and-cloud-infrastructure/
tags:
- veille-cyber
- hackernews
---
### Campagne Cyber Russe de Longue Haleine Visant des Infrastructures Critiques

Une campagne de cyberespionnage d'envergure, orchestrée par la Direction Principale du renseignement de l'état-major général des forces armées russes (GRU) et s'étendant sur plusieurs années (2021-2025), a été identifiée par Amazon. Elle cible des organisations des secteurs de l'énergie, des fournisseurs d'infrastructures critiques en Amérique du Nord et en Europe, ainsi que des entités utilisant des infrastructures réseau hébergées dans le cloud.

Cette campagne, également connue sous le nom d'APT44 ou Sandworm, se distingue par son utilisation de vecteurs d'accès initiaux axés sur des vulnérabilités de sécurité dans les dispositifs réseau périphériques mal configurés, plutôt que par l'exploitation de failles zero-day ou N-day, marquant ainsi une évolution tactique des acteurs malveillants. L'objectif est de récolter des identifiants et de se déplacer latéralement au sein des réseaux des victimes tout en minimisant le risque d'exposition.

**Points Clés :**

*   **Acteur :** GRU (Direction Principale du renseignement russe), également connu sous les noms APT44, FROZENBARENTS, Sandworm, Seashell Blizzard, Voodoo Bear.
*   **Cibles :** Secteur de l'énergie, infrastructures critiques, entités cloud.
*   **Période :** 2021-2025.
*   **Tactique principale :** Exploitation de dispositifs réseau périphériques mal configurés avec des interfaces de gestion exposées.
*   **Objectifs :** Récolte d'identifiants, mouvement latéral, accès persistant.
*   **Méthodologie :** Compromission des dispositifs périphériques, capture de trafic, vol d'identifiants, réutilisation d'identifiants contre les services en ligne des victimes.
*   **Chevauchement potentiel :** Infrastructure partagée avec le groupe Curly COMrades, suggérant une coordination plus large.

**Vulnérabilités exploitées (avec CVE si disponibles) :**

*   **2021-2022 :**
    *   Exploitation d'une faille dans les WatchGuard Firebox et XTM (CVE-2022-26318).
    *   Ciblage de dispositifs réseau périphériques mal configurés.
*   **2022-2023 :**
    *   Exploitation de vulnérabilités dans Atlassian Confluence (CVE-2021-26084, CVE-2023-22518).
    *   Poursuite du ciblage de dispositifs réseau périphériques mal configurés.
*   **2024 :**
    *   Exploitation d'une faille dans Veeam (CVE-2023-27532).
    *   Poursuite du ciblage de dispositifs réseau périphériques mal configurés.
*   **2025 :**
    *   Ciblage soutenu de dispositifs réseau périphériques mal configurés.

**Recommandations :**

*   Audit des dispositifs réseau périphériques pour détecter toute utilitaire de capture de paquets inattendu.
*   Mise en œuvre d'une authentification forte.
*   Surveillance des tentatives d'authentification provenant de localisations géographiques inhabituelles.
*   Surveillance active des attaques par réutilisation d'identifiants.

---
[Source](https://thehackernews.com/2025/12/amazon-exposes-years-long-gru-cyber.html){:target="_blank"}
