---
title: 'DarkSpectre Browser Extension Campaigns Exposed After Impacting 8.8 Million Users Worldwide'
date: 2025-12-31
permalink: /posts/2025/12/31/darkspectre-browser-extension-campaigns-exposed-after-impacting-88-million-users-worldwide/
tags:
- veille-cyber
- hackernews
---
## DarkSpectre : Campagnes d'extensions de navigateur malveillantes affectant 8,8 millions d'utilisateurs

Une campagne de logiciels malveillants ciblant les navigateurs web, attribuée à un acteur de menace chinois surnommé DarkSpectre, a eu un impact sur un total de 8,8 millions d'utilisateurs à travers trois campagnes distinctes s'étendant sur plus de sept ans. Ces campagnes incluent ShadyPanda, GhostPoster et The Zoom Stealer, et ont ciblé les utilisateurs de Google Chrome, Microsoft Edge et Mozilla Firefox.

**Points clés :**

*   **Objectif :** Vol de données, détournement de requêtes de recherche, fraude d'affiliation, injection de code de suivi et fraude publicitaire. La campagne The Zoom Stealer vise spécifiquement la collecte d'informations sur les réunions virtuelles d'entreprise.
*   **Méthode :** Distribution de fausses extensions de navigateur, souvent déguisées en outils utiles ou utilitaires VPN. Certaines extensions utilisent des "bombes logiques" pour retarder leur activation malveillante afin d'échapper à l'examen initial. D'autres restent "dormantes" pendant des années avant d'être activées par des mises à jour malveillantes.
*   **Impact :** Au total, plus de 8,8 millions d'utilisateurs ont été touchés. ShadyPanda a affecté 5,6 millions d'utilisateurs, GhostPoster a ciblé les utilisateurs de Firefox avec des utilitaires apparemment inoffensifs et des outils VPN, et The Zoom Stealer a touché environ 2,2 millions d'utilisateurs.
*   **Trafic de données :** Les informations collectées, notamment les liens de réunion avec mots de passe intégrés, les identifiants de réunion, les sujets, les descriptions, les heures planifiées et les statuts d'enregistrement, sont exfiltrées via une connexion WebSocket. Les données relatives aux intervenants et aux hôtes des webinaires, ainsi que les métadonnées de session, sont également collectées.
*   **Lien avec la Chine :** Les liens avec la Chine sont étayés par l'utilisation de serveurs de commande et de contrôle (C2) hébergés sur Alibaba Cloud, des enregistrements de fournisseurs de services Internet (ICP) liés à des provinces chinoises, des artefacts de code contenant des chaînes de caractères et des commentaires en chinois, et des schémas de fraude ciblant spécifiquement les plateformes de commerce électronique chinoises.
*   **Stratégie :** L'acteur de la menace semble adopter une approche à long terme, en créant des extensions apparemment légitimes pour bâtir la confiance, accumuler une base d'utilisateurs et gagner des badges avant de les rendre malveillantes.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article. Cependant, la nature même des extensions malveillantes exploite la confiance des utilisateurs dans les magasins d'extensions des navigateurs et la tendance à installer des outils sans vérification approfondie. La tactique de retardement des mises à jour malveillantes permet de contourner les mécanismes d'examen des extensions.

**Recommandations :**

*   **Prudence accrue :** Les utilisateurs doivent être extrêmement prudents lors de l'installation d'extensions de navigateur, même celles qui semblent légitimes ou qui proviennent de sources apparemment fiables.
*   **Vérification des autorisations :** Examiner attentivement les autorisations demandées par les extensions. Les extensions demandant un accès excessif à des plateformes de vidéoconférence, par exemple, devraient susciter la méfiance.
*   **Recherche avant installation :** Vérifier la réputation de l'extension et du développeur, lire les avis et rechercher des informations sur d'éventuels problèmes de sécurité avant de l'installer.
*   **Mises à jour régulières :** Maintenir les navigateurs et les extensions à jour peut aider à corriger les vulnérabilités connues.
*   **Suppression des extensions suspectes :** Les utilisateurs devraient supprimer proactivement toute extension dont ils n'ont pas un besoin immédiat ou dont l'utilité n'est pas claire.
*   **Surveillance des communications d'entreprise :** Pour les organisations, il est crucial de sensibiliser les employés aux risques liés aux extensions de navigateur et de mettre en place des politiques pour limiter l'installation d'extensions non autorisées, étant donné la nature de type "espionnage industriel" de certaines de ces menaces.

---
[Source](https://thehackernews.com/2025/12/darkspectre-browser-extension-campaigns.html){:target="_blank"}
