---
title: 'Exposed MongoDB instances still targeted in data extortion attacks'
date: 2026-02-01
permalink: /posts/2026/02/01/exposed-mongodb-instances-still-targeted-in-data-extortion-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Attaques de rançongiciels sur des instances MongoDB mal configurées**

Une menace récurrente cible des instances MongoDB exposées sur Internet, souvent non sécurisées par une mauvaise configuration. Ces attaques automatisées visent à extorquer de faibles rançons aux propriétaires des données compromises. Plus de 1 400 serveurs ont été affectés, les attaquants demandant environ 500 $ en Bitcoin pour restaurer les données. Cette pratique, qui avait atteint un pic jusqu'en 2021, continue à une échelle moindre, des chercheurs ayant découvert des centaines de milliers de serveurs MongoDB exposés, dont un grand nombre avec un accès non authentifié et près de la moitié déjà compromise.

Les notes de rançon exigent généralement un paiement en Bitcoin (environ 0,005 BTC) sous 48 heures, avec la promesse de restitution des données, bien qu'il n'y ait aucune garantie de succès. Les analyses révèlent un seul acteur malveillant principal derrière ces attaques, identifié par la prévalence d'une adresse de portefeuille Bitcoin unique.

Outre l'absence d'authentification, près de la moitié des serveurs exposés fonctionnent avec des versions obsolètes susceptibles de contenir des vulnérabilités connues. Bien que la plupart de ces failles soient limitées aux attaques par déni de service, elles ajoutent à la surface d'attaque globale.

**Points Clés :**

*   **Activité persistante :** Des attaques de rançongiciels continuent de cibler les bases de données MongoDB mal sécurisées.
*   **Motivation financière :** Les attaquants demandent de faibles rançons en Bitcoin pour la restauration des données.
*   **Volume d'exposition :** Un nombre important d'instances MongoDB restent exposées publiquement, certaines sans aucune authentification.
*   **Opérations simplifiées :** Un acteur unique semble mener la majorité de ces attaques.

**Vulnérabilités :**

*   **Mauvaise configuration :** Accès aux instances MongoDB sans restriction en raison d'une configuration incorrecte.
*   **Versions obsolètes :** Utilisation de versions de MongoDB comportant des failles connues (n-day flaws). L'article ne mentionne pas de CVEs spécifiques pour ces failles lors de l'identification des 95 000 instances obsolètes.

**Recommandations :**

*   **Limiter l'exposition publique :** Éviter de rendre les instances MongoDB accessibles publiquement sauf si cela est strictement nécessaire.
*   **Authentification forte :** Mettre en place des mesures d'authentification robustes.
*   **Contrôle d'accès réseau :** Utiliser des règles de pare-feu et des politiques réseau (par exemple, dans Kubernetes) pour n'autoriser que les connexions de confiance.
*   **Mise à jour régulière :** Maintenir MongoDB à jour avec la dernière version.
*   **Surveillance continue :** Surveiller activement l'exposition des instances et les journaux pour toute activité non autorisée.
*   **Rotation des identifiants :** Changer les identifiants en cas de suspicion d'exposition ou de compromission.
*   **Éviter les configurations par défaut :** Ne pas copier aveuglément les configurations des guides de déploiement.

---
[Source](https://www.bleepingcomputer.com/news/security/exposed-mongodb-instances-still-targeted-in-data-extortion-attacks/){:target="_blank"}
