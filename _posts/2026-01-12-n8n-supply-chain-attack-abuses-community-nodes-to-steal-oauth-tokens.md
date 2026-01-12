---
title: 'n8n Supply Chain Attack Abuses Community Nodes to Steal OAuth Tokens'
date: 2026-01-12
permalink: /posts/2026/01/12/n8n-supply-chain-attack-abuses-community-nodes-to-steal-oauth-tokens/
tags:
- veille-cyber
- hackernews
---
**Attaque par Chaîne d'Approvisionnement sur n8n : Vol de Jetons OAuth via des Nœuds Communautaires**

Une campagne malveillante a exploité l'écosystème de n8n, une plateforme d'automatisation de flux de travail, en publiant de faux nœuds communautaires sur le registre npm. Ces packages, se faisant passer pour des intégrations légitimes, visaient à dérober les identifiants OAuth des développeurs.

Un exemple typique est le package "n8n-nodes-hfgjf-irtuinvcm-lasdqewriit", qui simulait une intégration pour Google Ads. Il demandait aux utilisateurs de connecter leur compte publicitaire via un formulaire trompeur, avant d'exfiltrer les informations d'authentification vers des serveurs contrôlés par les attaquants. Cette attaque représente une nouvelle étape dans les menaces de chaîne d'approvisionnement, exploitant la confiance accordée aux intégrations pour accéder à des informations sensibles stockées dans des "coffres-forts" centralisés de jetons OAuth et clés API.

**Points Clés :**

*   Attaque de chaîne d'approvisionnement ciblant la plateforme d'automatisation de flux de travail n8n.
*   Utilisation de faux nœuds communautaires publiés sur npm pour tromper les utilisateurs.
*   Objectif principal : Voler des jetons OAuth et d'autres identifiants sensibles.
*   Les attaquants exploitent la confiance dans les intégrations pour accéder à des données critiques.
*   Les nœuds communautaires, s'ils sont compromis, disposent des mêmes privilèges que n8n lui-même, y compris l'accès aux clés API déchiffrées.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée dans l'article. L'attaque repose sur l'ingénierie sociale et la confiance accordée aux packages tiers. Le principal risque réside dans le manque de vérification et de sécurisation des nœuds communautaires.

**Recommandations :**

*   **Auditer les packages :** Les développeurs doivent examiner attentivement les packages avant de les installer.
*   **Vérifier les métadonnées :** Inspecter les informations relatives aux packages pour détecter toute anomalie.
*   **Privilégier les intégrations officielles :** Utiliser de préférence les intégrations fournies officiellement par n8n.
*   **Désactiver les nœuds communautaires (instances auto-hébergées) :** Pour les installations n8n auto-hébergées, il est conseillé de désactiver les nœuds communautaires en définissant la variable d'environnement `N8N_COMMUNITY_PACKAGES_ENABLED` sur `false`.

---
[Source](https://thehackernews.com/2026/01/n8n-supply-chain-attack-abuses.html){:target="_blank"}
