---
title: 'Amazon Disrupts APT29 Watering Hole Campaign Abusing Microsoft Device Code Authentication'
date: 2025-08-29
permalink: /posts/2025/08/29/amazon-disrupts-apt29-watering-hole-campaign-abusing-microsoft-device-code-authentication/
tags:
- veille-cyber
- hackernews
---
**APT29 Cible l'Authentification des Appareils Microsoft via une Campagne de Détournement**

Un groupe de hackers affilié à la Russie, connu sous le nom d'APT29 (également appelé Midnight Blizzard, The Dukes, etc.), a mené une campagne de "watering hole" visant à collecter des renseignements. Cette opération exploitait des sites web compromis pour rediriger les utilisateurs vers une infrastructure malveillante. L'objectif était d'inciter les victimes à autoriser des appareils contrôlés par les attaquants via le flux d'authentification de code d'appareil de Microsoft.

Cette technique permet aux acteurs malveillants d'obtenir un accès non autorisé aux comptes Microsoft 365 et aux données associées. Amazon a réussi à identifier et à perturber cette campagne, bien que les attaquants aient tenté de migrer vers de nouvelles infrastructures.

**Points Clés:**

*   **Acteur:** APT29 (Midnight Blizzard, The Dukes, etc.), groupe de hackers parrainé par l'État russe, lié au SVR.
*   **Méthode:** Campagne de "watering hole" utilisant des sites web compromis.
*   **Technique:** Détournement vers des pages falsifiées imitant des services légitimes (ex: Cloudflare) pour tromper les utilisateurs.
*   **Exploitation:** Le flux d'authentification de code d'appareil de Microsoft pour obtenir l'autorisation d'accéder aux comptes.
*   **Objectif:** Collecte de renseignements et vol d'identifiants.
*   **Évolution:** APT29 adapte ses méthodes, incluant le phishing par code d'appareil et le "device join phishing" pour accéder aux comptes Microsoft 365.
*   **Techniques d'Évasion:** Utilisation de l'encodage Base64, de cookies pour éviter les redirections répétées et déplacement vers de nouvelles infrastructures en cas de blocage.
*   **Intervention:** Amazon a identifié et perturbé la campagne, malgré les tentatives de migration des attaquants.

**Vulnérabilités:**

L'article ne mentionne pas de CVE spécifiques pour cette campagne. La vulnérabilité exploitée réside dans la conception de flux d'authentification qui, s'ils ne sont pas correctement protégés contre la manipulation par des tiers, peuvent être détournés pour autoriser des accès non désirés.

**Recommandations:**

Bien que l'article ne fournisse pas de recommandations directes, des pratiques de sécurité générales s'appliquent pour se protéger contre ce type d'attaques :

*   **Vigilance accrue:** Se méfier des redirections inattendues depuis des sites web légitimes.
*   **Vérification des URLs:** S'assurer que les URL des pages de connexion et d'authentification sont légitimes avant de saisir des informations.
*   **Authentification Multi-Facteurs (MFA):** Activer et utiliser la MFA sur tous les comptes, en particulier ceux de Microsoft 365, pour une couche de sécurité supplémentaire.
*   **Éducation à la sécurité:** Sensibiliser les utilisateurs aux techniques de phishing et d'ingénierie sociale.
*   **Surveillance des accès:** Examiner régulièrement les appareils et les sessions actives liés aux comptes pour détecter toute activité suspecte.

---
[Source](https://thehackernews.com/2025/08/amazon-disrupts-apt29-watering-hole.html){:target="_blank"}
