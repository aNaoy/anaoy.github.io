---
title: 'How to Streamline Zero Trust Using the Shared Signals Framework'
date: 2025-12-09
permalink: /posts/2025/12/09/how-to-streamline-zero-trust-using-the-shared-signals-framework/
tags:
- veille-cyber
- hackernews
---
### Optimiser la Confiance Zéro avec le Cadre de Signaux Partagés

L'implémentation du modèle de Confiance Zéro (Zero Trust) est souvent entravée par le manque d'interopérabilité entre les outils de sécurité, qui peinent à échanger des signaux de manière fiable. Cela empêche la prise de décisions d'accès en temps réel et complique l'application cohérente des politiques de sécurité. Un pourcentage élevé d'organisations reconnaît avoir rencontré des difficultés significatives dans l'adoption de ces approches.

Scott Bean, ingénieur senior chez MongoDB, a proposé une solution pour fluidifier l'utilisation du Cadre de Signaux Partagés (Shared Signals Framework - SSF) en créant un "émetteur" SSF. Ce système permet aux outils qui ne supportent pas nativement le SSF, comme Kolide Device Trust, d'envoyer des signaux à des plateformes comme Okta. En utilisant la plateforme Tines comme orchestrateur, les problèmes de conformité des appareils détectés par Kolide peuvent être transformés en événements CAEP (Continuous Access Evaluation Protocol) au format SET (Security Event Token), puis transmis à Okta.

Ce mécanisme assure que même si un outil n'est pas conçu pour le SSF, ses informations de sécurité peuvent être standardisées et transmises. Tines agit comme un pont, permettant de recevoir, enrichir, corréler, générer et signer des SETs conformes aux spécifications SSF, avant de les livrer aux fournisseurs d'identité. Cela aboutit à une évaluation des risques des appareils plus rapide et plus fiable, une meilleure réactivité face aux menaces, et une orchestration de politiques plus flexible.

**Points clés :**

*   Le manque de support natif du SSF par de nombreux outils de sécurité complique la mise en œuvre du Zero Trust.
*   Le SSF vise à standardiser l'échange d'événements de sécurité.
*   Tines peut servir de médiateur pour intégrer des outils comme Kolide Device Trust avec des plateformes comme Okta via le SSF.
*   La solution transforme les problèmes de conformité des appareils en événements CAEP (SETs) compréhensibles par Okta.

**Vulnérabilités adressées (implicitement) :**

*   Les décisions d'accès obsolètes dues à des signaux de sécurité non partagés en temps réel.
*   L'incapacité d'appliquer des politiques de sécurité cohérentes sur l'ensemble de l'environnement.
*   Les lacunes dans l'évaluation continue de la posture des appareils.

**Recommandations :**

*   Utiliser des plateformes d'orchestration comme Tines pour combler les lacunes d'interopérabilité SSF.
*   Mettre en place un flux de travail pour générer, signer et transmettre des événements de sécurité standardisés (SETs) aux fournisseurs d'identité.
*   Déployer des "émetteurs" SSF pour permettre aux outils ne supportant pas nativement le standard de participer à l'écosystème SSF.
*   Exploiter les capacités de Tines pour recevoir des signaux (par webhook), enrichir les données, générer des tokens conformes au SSF, et les envoyer à Okta (ou autres) pour renforcer les politiques Zero Trust.

---
[Source](https://thehackernews.com/2025/12/how-to-streamline-zero-trust-using.html){:target="_blank"}
