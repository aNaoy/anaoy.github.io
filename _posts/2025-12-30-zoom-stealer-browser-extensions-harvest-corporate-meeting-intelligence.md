---
title: 'Zoom Stealer browser extensions harvest corporate meeting intelligence'
date: 2025-12-30
permalink: /posts/2025/12/30/zoom-stealer-browser-extensions-harvest-corporate-meeting-intelligence/
tags:
- veille-cyber
- bleepingcomp
---
### Extension de navigateur : une menace pour la confidentialité des réunions en ligne

Une campagne malveillante, baptisée "Zoom Stealer", a compromis environ 2,2 millions d'utilisateurs de navigateurs Chrome, Firefox et Microsoft Edge via 18 extensions. Ces extensions, conçues pour collecter des informations relatives aux réunions en ligne, visent à obtenir des détails tels que les URL, les identifiants de réunion, les sujets, les descriptions et même les mots de passe intégrés.

Ces extensions fonctionnent de manière légitime pour l'utilisateur, collectant des données sur 28 plateformes de visioconférence populaires (Zoom, Microsoft Teams, Google Meet, Cisco WebEx, etc.). Les informations dérobées incluent les liens de réunion et leurs identifiants, les statuts d'enregistrement, les titres, les noms des intervenants et des hôtes, ainsi que des métadonnées de session. Ces données sont ensuite transmises en temps réel aux acteurs malveillants.

Cette campagne est attribuée à un acteur de menace unique, connu sous le nom de DarkSpectre, qui serait lié à la Chine. DarkSpectre est également derrière des campagnes antérieures, GhostPoster et ShadyPanda, qui ont affecté des millions d'utilisateurs. L'infrastructure utilisée, les commentaires en chinois dans le code et les schémas d'activité correspondent à des indices indiquant une origine chinoise.

Les informations collectées peuvent être exploitées pour de l'espionnage industriel, de l'intelligence commerciale, des attaques d'ingénierie sociale, voire vendues à des concurrents. La création d'une base de données à grande échelle permettrait des opérations d'usurpation d'identité complexes, fournissant des identifiants pour rejoindre des appels confidentiels, des listes de participants et un contexte pour rendre les impersonations crédibles.

Bien que les extensions malveillantes aient été signalées, certaines sont encore disponibles sur les boutiques d'extensions de navigateurs.

**Points clés :**

*   **Nom de la campagne :** Zoom Stealer
*   **Acteur de menace :** DarkSpectre (associé à la Chine)
*   **Cibles :** Utilisateurs de Chrome, Firefox, Microsoft Edge
*   **Nombre d'utilisateurs affectés :** Environ 2,2 millions par Zoom Stealer ; plus de 7,8 millions sur sept ans par les campagnes de DarkSpectre.
*   **Méthode :** 18 extensions de navigateur, initialement fonctionnelles.
*   **Données collectées :** URL de réunion, identifiants (y compris les mots de passe intégrés), sujets, descriptions, statuts d'enregistrement, informations sur les intervenants et les hôtes, métadonnées de session.
*   **Objectifs potentiels :** Espionnage industriel, intelligence commerciale, usurpation d'identité, attaques par ingénierie sociale.

**Vulnérabilités :**

*   Non spécifié de CVE dans l'article. Les vulnérabilités résident dans les autorisations excessives demandées par les extensions et leur capacité à collecter des données sensibles sans consentement explicite pour l'usage malveillant.

**Recommandations :**

*   Examiner attentivement les autorisations demandées par les extensions de navigateur.
*   Limiter le nombre d'extensions installées au strict nécessaire.
*   Désinstaller les extensions suspectes ou inutiles.
*   Être vigilant face aux extensions qui demandent des accès étendus aux plateformes de communication.

---
[Source](https://www.bleepingcomputer.com/news/security/zoom-stealer-browser-extensions-harvest-corporate-meeting-intelligence/){:target="_blank"}
