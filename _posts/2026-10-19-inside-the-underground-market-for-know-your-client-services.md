---
title: 'Inside the Underground Market for Know Your Client Services'
date: 2026-10-19
permalink: /posts/2026/10/19/inside-the-underground-market-for-know-your-client-services/
tags:
- veille-cyber
- bleepingcomp
---
### Le marché souterrain des services de fraude KYC

Le secteur de la cybercriminalité a industrialisé le contournement des procédures « Know Your Client » (KYC) imposées aux institutions financières. Des plateformes proposent désormais des packages complets incluant de faux documents d'identité (passeports, permis, relevés bancaires) et des outils pour tromper la vérification biométrique en temps réel.

**Points clés :**
*   **Offres groupées :** Les fraudeurs ne vendent plus seulement de faux documents, mais des identités numériques cohérentes (« identity packages ») conçues pour passer les contrôles des banques et plateformes de cryptomonnaies.
*   **Techniques de contournement :** Utilisation de *deepfakes* pour altérer les flux vidéo lors de vérifications en direct, logiciels de remplacement de caméra (virtual cameras) et recours à des opérateurs humains pour réussir les tests de vivacité (*liveness checks*).
*   **Maintenance post-fraude :** Les vendeurs assurent un support continu, notamment pour franchir des étapes de vérification supplémentaires après l'ouverture initiale du compte.

**Vulnérabilités :**
Cet article ne liste pas de CVE spécifiques, car il s'agit d'une menace liée à l'ingénierie sociale et à l'abus de processus métier plutôt qu'à une faille logicielle unique. Les vulnérabilités résident dans :
*   La dépendance excessive aux systèmes de vérification automatisés sans analyse de cohérence globale.
*   L'incapacité de certains systèmes de contrôle à détecter l'injection de flux vidéo virtuels ou les outils de modification d'apparence en temps réel.

**Recommandations :**
*   **Approche holistique :** Ne pas se limiter à la vérification d'un document isolé. Croiser les données d'identité, les relevés fournis, les images faciales et l'activité de l'utilisateur pour détecter des incohérences.
*   **Contrôles dynamiques :** Imposer des instructions imprévisibles lors des tests de vivacité (ex: lecture de chiffres aléatoires, mouvements spécifiques) pour rendre l'utilisation de vidéos pré-enregistrées ou de deepfakes statiques plus complexe.
*   **Analyse de contexte :** Collecter et analyser les métadonnées de l'appareil (device fingerprinting) lors de la session pour vérifier si l'équipement est conforme aux standards attendus.
*   **Veille proactive :** Surveiller les forums spécialisés pour identifier les fuites de données personnelles ou les services ciblant spécifiquement votre organisation.

---
[Source](https://www.bleepingcomputer.com/news/security/inside-the-underground-market-for-know-your-client-services/){:target="_blank"}
