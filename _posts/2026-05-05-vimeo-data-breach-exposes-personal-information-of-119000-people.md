---
title: 'Vimeo data breach exposes personal information of 119,000 people'
date: 2026-05-05
permalink: /posts/2026/05/05/vimeo-data-breach-exposes-personal-information-of-119000-people/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez Vimeo : 119 000 utilisateurs exposés via Anodot

La plateforme Vimeo a été victime d'une fuite de données suite à un piratage ciblant son partenaire, la société d'analyse de données Anodot. Le groupe de cybercriminels *ShinyHunters* a récupéré et publié une archive de 106 Go sur le dark web après l'échec d'une tentative d'extorsion envers Vimeo.

**Points clés :**
*   **Impact :** Environ 119 200 personnes sont concernées.
*   **Données compromises :** Informations techniques, titres de vidéos, métadonnées, noms et adresses e-mail.
*   **Données sécurisées :** Les identifiants de connexion (mots de passe), les informations de paiement et le contenu vidéo réel n'ont pas été compromis.
*   **Mode opératoire :** Les attaquants ont exploité des jetons d'authentification Anodot pour accéder aux instances Snowflake et BigQuery de Vimeo.

**Vulnérabilités :**
*   Le vecteur d'attaque repose sur une compromission de la chaîne d'approvisionnement logicielle (*Supply Chain Attack*). Aucun identifiant CVE spécifique n'est associé à cette intrusion, celle-ci étant liée à une mauvaise gestion ou au vol de jetons d'accès SaaS tiers.

**Recommandations :**
*   **Audit des accès tiers :** Révoquer systématiquement les jetons d'authentification et les accès API inutilisés ou obsolètes accordés à des fournisseurs tiers.
*   **Gestion des intégrations SaaS :** Limiter les privilèges des intégrations tierces (principe du moindre privilège) pour éviter qu'une compromission chez un partenaire ne donne accès à l'intégralité des instances de données (type Snowflake ou BigQuery).
*   **Surveillance :** Mettre en œuvre des systèmes de détection d'anomalies basés sur l'IA pour repérer les comportements suspects lors de l'utilisation d'identifiants de services tiers, comme ce fut le cas pour bloquer les tentatives sur Salesforce.
*   **Réponse aux incidents :** En cas de compromission, isoler immédiatement le système impacté et supprimer les intégrations avec le partenaire vulnérable.

---
[Source](https://www.bleepingcomputer.com/news/security/vimeo-data-breach-exposes-personal-information-of-119-000-people/){:target="_blank"}
