---
title: '1Campaign platform helps malicious Google ads evade detection'
date: 2026-02-25
permalink: /posts/2026/02/25/1campaign-platform-helps-malicious-google-ads-evade-detection/
tags:
- veille-cyber
- bleepingcomp
---
**1Campaign : La Plateforme d'Évasion des Publicités Malveillantes sur Google**

Une nouvelle plateforme de cybercriminalité, baptisée 1Campaign, permet aux acteurs malveillants de déployer des publicités sur Google qui échappent durablement aux détections et à l'examen des chercheurs en sécurité. Ce service de "cloaking" fait passer le contenu malveillant par les filtres de Google, ne le présentant qu'aux véritables victimes potentielles. Les chercheurs et les scanners automatisés, eux, ne voient que des pages blanches inoffensives.

Développée par un individu se présentant comme 'DuppyMeister' et active depuis au moins trois ans, 1Campaign offre un tableau de bord convivial pour gérer les campagnes. Le système filtre les visiteurs en temps réel en fonction de critères tels que la géographie, le fournisseur d'accès à Internet (FAI) et les caractéristiques de l'appareil. Cette approche ciblée permet aux attaquants de se concentrer sur les régions les plus réceptives à leurs leurres de phishing et de crypto-drainers, tout en évitant les zones susceptibles de faire l'objet d'une surveillance accrue. Le système attribue un score de risque de fraude aux visiteurs, bloquant automatiquement ceux provenant de fournisseurs cloud majeurs, de centres de données, de VPN ou de fournisseurs de sécurité. Il peut également identifier les scanners de sécurité grâce à l'analyse des adresses IP, des FAI et des comportements.

La plateforme facilite également le contournement des limitations de politique de Google et l'usurpation d'identité de marques légitimes via un outil de lancement de campagnes publicitaires. Bien que Google déploie des mesures de sécurité, 1Campaign se distingue par sa conception spécifique pour lancer des publicités malveillantes qui réussissent les inspections automatiques et persistent jusqu'à signalement manuel par les victimes ou par des tiers.

**Points Clés :**

*   **Cloaking Avancé :** 1Campaign dissimule le contenu malveillant des publicités pour ne le montrer qu'aux utilisateurs ciblés, présentant des pages bénignes aux systèmes de sécurité.
*   **Filtrage Intelligent :** Le service utilise la géographie, le FAI, les caractéristiques de l'appareil et une évaluation du risque de fraude pour cibler les victimes et bloquer les investigateurs.
*   **Persistance des Campagnes :** Les publicités malveillantes conçues avec 1Campaign parviennent à rester en ligne plus longtemps, échappant aux mécanismes de détection courants.
*   **Outil d'Usurpation :** La plateforme inclut une fonction pour aider à contourner les politiques de Google Ads et à imiter des marques légitimes.

**Vulnérabilités / Menaces :**

*   **Évasion de la Détection :** Le principal problème est la capacité de 1Campaign à déjouer les systèmes de sécurité et de modération de Google Ads.
*   **Phishing et Vol de Crypto :** Les publicités malveillantes visent à tromper les utilisateurs pour voler leurs identifiants ou leurs cryptomonnaies.
*   **Impact sur la Confiance :** L'efficacité de telles plateformes nuit à la confiance des utilisateurs dans les résultats de recherche sponsorisés.

**Recommandations :**

*   **Prudence avec les Résultats Sponsorisés :** Éviter les résultats promus sur les moteurs de recherche ou les traiter avec une extrême suspicion.
*   **Vérification des URL :** Toujours vérifier attentivement l'adresse URL dans la barre du navigateur avant de saisir des informations sensibles.
*   **Favoriser les Sources Officielles :** Utiliser des canaux de distribution de logiciels officiels et de confiance.
*   **Détection Améliorée (pour les professionnels) :** Utiliser des empreintes de navigateur réalistes et des interactions simulant l'activité humaine pour une meilleure analyse.
*   **Rotation des Identifiants (pour les professionnels) :** Pour la détection automatisée, alterner les adresses IP et les configurations d'user-agent afin d'éviter une empreinte numérique cohérente.

---
[Source](https://www.bleepingcomputer.com/news/security/1campaign-platform-helps-malicious-google-ads-evade-detection/){:target="_blank"}
