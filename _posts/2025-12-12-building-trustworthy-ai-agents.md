---
title: 'Building Trustworthy AI Agents'
date: 2025-12-12
permalink: /posts/2025/12/12/building-trustworthy-ai-agents/
tags:
- veille-cyber
- schneier
---
### Pour une IA personnelle digne de confiance

Les assistants IA personnels actuels posent des risques significatifs en raison d'un manque d'intégrité des données. Ils peuvent induire en erreur, manipuler les utilisateurs et ne pas gérer correctement le contexte incomplet ou inexact. Ce problème est amplifié par le besoin d'accès à des données personnelles intimes pour la personnalisation de l'IA.

Pour remédier à cela, il est proposé de séparer les magasins de données personnelles des systèmes d'IA. Cette approche permet aux avancées en matière de sécurité de progresser indépendamment de celles de l'IA.

Un magasin de données personnel digne de confiance devrait répondre à six exigences clés, en plaçant l'intégrité au centre de la sécurité :

*   **Accessibilité en tant que référentiel de données :** Inclure des données personnelles, des transactions et des interactions, qu'elles soient brutes ou traitées.
*   **Accessibilité en tant que source de données :** Permettre à différents modèles d'IA d'accéder et d'utiliser ces données, sans être lié à un seul modèle.
*   **Capacité à prouver l'exactitude des données :** Fournir une preuve de complétude et d'exactitude des données pour des applications critiques (par exemple, négociations, entretiens d'embauche).
*   **Contrôle granulaire et audit par l'utilisateur :** L'utilisateur doit avoir un contrôle total sur qui accède à quelles données et sous quelles conditions, avec la possibilité de révoquer rapidement l'accès et d'auditer les accès passés.
*   **Sécurité :** Protection robuste contre les attaques en lecture (pour apprendre les données) et en écriture (pour modifier ou ajouter des données), nécessitant un système d'authentification complexe.
*   **Facilité d'utilisation :** L'interface doit être intuitive et ne pas nécessiter de formation spécialisée en sécurité pour l'utilisateur moyen.

Cette approche, qui s'inspire de concepts comme le "Human Context Protocol" et le protocole Solid de Tim Berners-Lee, vise à doter les utilisateurs de la propriété et du contrôle de leurs données. Cela permettrait aux IA de ne pas manipuler facilement les utilisateurs, car ces derniers auraient une vision claire des données utilisées et la capacité de corriger les informations erronées ou contextuelles. La séparation des expertises en IA et en sécurité des données est considérée comme essentielle pour construire des assistants IA réellement dignes de confiance.

**Points clés :**

*   Les IA personnelles actuelles manquent d'intégrité des données, menant à des risques de manipulation et d'erreurs.
*   La personnalisation de l'IA nécessite un accès intime aux données personnelles, accentuant le besoin de confiance.
*   La séparation des magasins de données personnels des systèmes d'IA est cruciale pour la sécurité.
*   L'intégrité des données est le principe directeur pour rendre l'IA digne de confiance.

**Vulnérabilités (implicites dans l'article, sans CVE spécifiques mentionnés) :**

*   Manipulation des utilisateurs par des données inexactes ou trompeuses.
*   "Gaslighting" par l'IA, remettant en question la perception de la réalité par l'utilisateur.
*   Incapacité à distinguer l'identité actuelle de l'identité passée de l'utilisateur.
*   Gestion inadéquate du contexte incomplet, inexact ou partiel.
*   Manque de mécanismes pour corriger les erreurs ou assurer la responsabilité.
*   Attaques en lecture sur les données personnelles.
*   Attaques en écriture visant à modifier ou corrompre les données personnelles.

**Recommandations :**

*   **Séparer les magasins de données personnels des systèmes d'IA.**
*   Développer des systèmes de données personnels répondant aux critères suivants : accessibilité, preuve d'exactitude, contrôle granulaire par l'utilisateur, sécurité robuste et facilité d'utilisation.
*   Investir dans l'expertise en sécurité des données, distincte de celle du développement d'IA.
*   Mettre en œuvre des systèmes d'authentification complexes pour protéger les données.
*   Favoriser des protocoles comme le "Human Context Protocol" ou des extensions de Solid pour la gestion des données personnelles.

---
[Source](https://www.schneier.com/blog/archives/2025/12/building-trustworthy-ai-agents.html){:target="_blank"}
