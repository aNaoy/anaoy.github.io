---
title: 'Taiwan-Based Hacker Used BOSSAI AI Agents to Steal Taipei Emergency Dispatch Records'
date: 2026-11-09
permalink: /posts/2026/11/09/taiwan-based-hacker-used-bossai-ai-agents-to-steal-taipei-emergency-dispatch-records/
tags:
- veille-cyber
- hackernews
---
### Attaque par agents IA : Compromission des services d'urgence à Taïwan

Un attaquant basé à Taïwan a utilisé un système multi-agents nommé **BOSSAI** pour cibler des centaines d'organisations dans 11 pays, notamment dans les secteurs des services d'urgence, bancaire, universitaire et militaire. En s'appuyant sur des modèles d'IA "ablitérés" (modèles locaux débarrassés de leurs garde-fous éthiques), l'attaquant a réussi à exfiltrer des dossiers de répartition des secours à Taipei et des données médicales exposées depuis 2018.

#### Points clés
*   **Mode opératoire :** Utilisation de 9 à 12 agents IA automatisant la reconnaissance, le scan et l'exploitation de vulnérabilités.
*   **Infrastructure :** L'attaquant a utilisé son propre serveur de développement comme plateforme d'attaque opérationnelle, laissant fuiter plus de 90 000 fichiers (logs, outils, identifiants).
*   **Efficacité limitée :** L'IA a surtout réussi à exploiter des systèmes mal configurés ou obsolètes. Les mécanismes de défense classiques (authentification forte, filtrage d'endpoints) ont bloqué la progression des agents.
*   **Attribution :** La négligence de l'opérateur (réutilisation d'identités, adresse IP personnelle exposée via SSH) a permis aux chercheurs d'Acronis d'identifier un individu unique résidant à Hualien, Taïwan.

#### Vulnérabilités exploitées
*   **Défaut de configuration :** Accès à des bases de données via des identifiants par défaut (`root`).
*   **Exposition de secrets :** Clés AES-256 codées en dur dans le JavaScript front-end, permettant le détournement de sessions.
*   **Injection SQL :** Présence de vulnérabilités d'injection sur des serveurs de prêts et universitaires.
*   **Plateformes obsolètes :** Accès sans authentification à des plateformes médicales datant de 2018.
*   **CVE :** Le rapport mentionne l'utilisation de scans pour des vulnérabilités Apache (RCE), bien que certains résultats aient été identifiés comme des faux positifs par l'IA elle-même.

#### Recommandations
*   **Gestion des accès :** Supprimer impérativement les identifiants par défaut sur tous les panels d'administration et les bases de données.
*   **Sécurisation du code :** Éliminer les clés API ou de chiffrement codées en dur dans le code source (côté client).
*   **Hygiène réseau :** Appliquer une politique stricte de filtrage des endpoints et s'assurer que les API exposées ne délivrent pas de données sensibles sans authentification forte.
*   **Mise à jour et audit :** Décommissionner les anciens serveurs (comme celui de 2018) et auditer régulièrement les bases de données pour prévenir les injections SQL.
*   **Protection des modèles IA :** Bien que l'IA facilite les attaques, la défense repose sur les fondamentaux de la cybersécurité : le patch management, l'authentification multi-facteurs (MFA) et la réduction de la surface d'attaque.

---
[Source](https://thehackernews.com/2026/11/taiwan-based-hacker-used-bossai-ai.html){:target="_blank"}
