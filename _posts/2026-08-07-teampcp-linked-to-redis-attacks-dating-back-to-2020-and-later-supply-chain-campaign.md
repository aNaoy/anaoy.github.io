---
title: 'TeamPCP Linked To Redis Attacks Dating Back To 2020 And Later Supply Chain Campaign'
date: 2026-08-07
permalink: /posts/2026/08/07/teampcp-linked-to-redis-attacks-dating-back-to-2020-and-later-supply-chain-campaign/
tags:
- veille-cyber
- hackernews
---
### L'évolution stratégique du groupe cybercriminel TeamPCP

Des recherches récentes révèlent que le groupe **TeamPCP** n'est pas une entité nouvelle, mais une évolution d'un écosystème malveillant actif depuis 2020. Initialement spécialisé dans l'exploitation d'infrastructures exposées (Redis, Docker, Ray), le groupe a progressivement étendu ses capacités vers des attaques sophistiquées contre la chaîne d'approvisionnement logicielle et des environnements cloud natifs.

**Points clés :**
*   **Continuité opérationnelle :** Les campagnes *ShadowRay 2.0* et *TA-NATALSTATUS* sont directement liées aux activités historiques du groupe, partageant infrastructures de commande et contrôle (C2), méthodes d'exfiltration et techniques de déploiement de malwares.
*   **Diversification des méfaits :** Leurs objectifs incluent le minage de cryptomonnaies, l'espionnage, le déploiement de ransomwares et la création de botnets de type "proxy" distribués.
*   **Capacités destructrices :** L'usage de scripts avancés (ex: *kube.py*) permet désormais d'inclure des fonctionnalités de type "wiper" (effacement de données), ciblant spécifiquement certains systèmes par géolocalisation.
*   **Mutation vers la supply chain :** Le groupe utilise désormais le vol de jetons d'accès et le détournement de GitHub Actions pour empoisonner des bibliothèques open-source, infectant ainsi massivement les systèmes des développeurs.

**Vulnérabilités exploitées :**
Le groupe s'appuie sur une exploitation récurrente de failles connues dans des technologies largement déployées, notamment :
*   **Redis :** Exploitation de serveurs mal configurés/exposés.
*   **React / Next.js :** Exploitation de vulnérabilités dans les composants serveur (RSC) (ex: *Operation PCPcat*).
*   **Ray / Docker :** Exploitation de failles non corrigées pour permettre la propagation de vers informatiques.

**Recommandations :**
*   **Durcissement des accès :** Sécuriser strictement les instances Redis, Docker et les clusters Kubernetes (limiter l'exposition Internet, utiliser des politiques de moindre privilège).
*   **Gestion des identités :** Protéger les jetons d'accès et les secrets utilisés dans les pipelines CI/CD (GitHub Actions, GitLab) pour prévenir l'empoisonnement de la supply chain.
*   **Veille et correctifs :** Appliquer systématiquement les correctifs de sécurité sur les frameworks web (React, Next.js) et les outils d'infrastructure.
*   **Monitoring :** Surveiller les comportements anormaux au sein des clusters Kubernetes, notamment les exécutions de scripts Python suspects ou les tentatives de modification de la configuration des nœuds.

---
[Source](https://thehackernews.com/2026/08/teampcp-linked-to-redis-attacks-dating.html){:target="_blank"}
