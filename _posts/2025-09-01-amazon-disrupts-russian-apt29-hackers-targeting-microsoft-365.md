---
title: 'Amazon disrupts Russian APT29 hackers targeting Microsoft 365'
date: 2025-09-01
permalink: /posts/2025/09/01/amazon-disrupts-russian-apt29-hackers-targeting-microsoft-365/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne de phishing sophistiquée déjouée : APT29 ciblé sur Microsoft 365**

Une opération de cybercriminalité attribuée au groupe russe Midnight Blizzard (également connu sous le nom d'APT29) a été perturbée. Ce groupe, lié au Service russe de renseignement extérieur (SVR), visait à obtenir l'accès aux comptes et aux données Microsoft 365 par le biais d'une campagne de "watering hole".

Les pirates ont compromis des sites web légitimes pour rediriger un sous-ensemble d'utilisateurs vers une infrastructure malveillante. Ces derniers étaient incités à autoriser des appareils contrôlés par l'attaquant via un flux d'authentification de code d'appareil Microsoft. Pour ce faire, des domaines imitant des pages de vérification Cloudflare ont été utilisés, certains visiteurs étant redirigés aléatoirement. Le groupe a mis en œuvre un système de cookies pour éviter les redirections multiples d'un même utilisateur, réduisant ainsi les soupçons.

Cette campagne représente une évolution des méthodes d'APT29, abandonnant les techniques d'usurpation d'identité de services cloud ou les tentatives d'ingénierie sociale pour contourner l'authentification multifacteur (MFA).

**Points clés :**

*   **Attaque :** Campagne de "watering hole" visant Microsoft 365.
*   **Acteur :** Midnight Blizzard (APT29), groupe soutenu par la Russie.
*   **Méthode :** Compromission de sites légitimes, redirection vers des faux portails de vérification Cloudflare, utilisation de l'authentification par code d'appareil Microsoft pour voler des identifiants.
*   **Évolution :** Abandon des anciennes techniques d'usurpation d'identité et d'ingénierie sociale pour le contournement de la MFA.

**Vulnérabilités (non spécifiées avec des CVEs dans l'article) :**

*   Utilisation de flux d'authentification de code d'appareil pour l'autorisation de périphériques malveillants.
*   Potentielle faible sensibilisation des utilisateurs aux requêtes d'autorisation d'appareils inhabituelles.

**Recommandations :**

*   **Pour les utilisateurs :** Vérifier systématiquement les demandes d'autorisation d'appareils, activer l'authentification multifacteur (MFA), et s'abstenir d'exécuter des commandes copiées depuis des pages web.
*   **Pour les administrateurs :** Désactiver les flux d'autorisation d'appareils non nécessaires lorsque possible, appliquer des politiques d'accès conditionnel, et surveiller activement les événements d'authentification suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/amazon-disrupts-russian-apt29-hackers-targeting-microsoft-365/){:target="_blank"}
