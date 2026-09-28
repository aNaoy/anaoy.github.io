---
title: 'Dutch Police Arrest ‘Reformed’ Hacker in Shiny Hunters Investigation'
date: 2026-09-28
permalink: /posts/2026/09/28/dutch-police-arrest-reformed-hacker-in-shiny-hunters-investigation/
tags:
- veille-cyber
- krebs
---
### Arrestation liée au groupe ShinyHunters et escalade des cyberattaques

Les autorités néerlandaises ont arrêté Pepijn van der Stap, un hacker récidiviste connu sous le pseudonyme « Umbreon », pour son implication présumée dans les activités du groupe criminel **ShinyHunters**. Cette arrestation a provoqué une réaction agressive de la part du groupe, qui a intensifié ses cyberattaques, notamment contre le FBI, tout en tentant d'incriminer le suspect néerlandais via des signatures numériques liées à son passé.

#### Points clés
*   **Conflit interne et leadership :** Le groupe ShinyHunters a fusionné avec d'autres entités criminelles (Scattered Spider, LAPSUS$) pour former le collectif **ScatteredLapsussHunters (SLSH)**, dirigé par un adolescent jordanien surnommé « Rey ».
*   **Tactiques de sabotage :** Le groupe actuel a utilisé l'image de marque d'« Umbreon » (le personnage Pokémon) lors du piratage du site de recrutement du FBI afin de détourner les soupçons vers le hacker néerlandais récemment arrêté.
*   **Vol d'ampleur :** ShinyHunters a détourné des données sensibles de plus de 6,2 millions de citoyens néerlandais chez l'opérateur Odido et a dérobé des informations personnelles (incluant des dossiers médicaux et psychiatriques) de plus de 5 000 employés du FBI.
*   **Efficacité financière :** Le groupe est extrêmement lucratif, avec des revenus d'extorsion estimés à près de 100 millions de dollars pour l'année 2026.

#### Vulnérabilités exploitées
*   **CVE-2026-35273 :** Une faille critique dans la plateforme **Oracle PeopleSoft**. Bien qu'un correctif ait été publié par Oracle, le groupe a contourné les règles de filtrage (WAF) recommandées par Mandiant en utilisant des techniques d'encodage d'URL pour exploiter massivement cette vulnérabilité.
*   **Ingénierie sociale :** Le groupe utilise le "vishing" (fraude par téléphone) pour convaincre des employés de se connecter à des sites miroirs malveillants afin de dérober leurs identifiants.

#### Recommandations
*   **Correction logicielle :** Appliquer immédiatement les correctifs de sécurité fournis par Oracle pour PeopleSoft. Le simple filtrage WAF s'est avéré insuffisant face aux techniques de contournement avancées.
*   **Renforcement de l'authentification :** En raison de la recrudescence d'attaques par ingénierie sociale, l'implémentation d'une authentification multifacteur (MFA) résistante au phishing (clés matérielles FIDO2/WebAuthn) est indispensable pour protéger les accès distants et les portails RH.
*   **Surveillance proactive :** Les organisations utilisant des plateformes de gestion des ressources humaines (SaaS) doivent surveiller étroitement les logs d'accès pour détecter des tentatives de contournement de WAF via des caractères encodés (URL encoding).

---
[Source](https://krebsonsecurity.com/2026/09/dutch-police-arrest-reformed-hacker-in-shiny-hunters-investigation/){:target="_blank"}
