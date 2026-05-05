---
title: 'FTC to ban data broker Kochava from selling Americans’ location data'
date: 2026-05-05
permalink: /posts/2026/05/05/ftc-to-ban-data-broker-kochava-from-selling-americans-location-data/
tags:
- veille-cyber
- bleepingcomp
---
### Restriction des courtiers en données : Le cas Kochava

La Federal Trade Commission (FTC) a conclu un accord avec le courtier en données Kochava et sa filiale Collective Data Solutions (CDS), leur interdisant de vendre ou de partager des données de géolocalisation précises sans le consentement explicite des utilisateurs. Cette mesure fait suite à une plainte déposée en 2022 dénonçant la commercialisation de données permettant de suivre les déplacements des citoyens vers des lieux sensibles (cliniques de santé reproductive, centres de désintoxication, lieux de culte, refuges).

**Points clés :**
* **Pratique illicite :** Kochava commercialisait, via l'AWS Marketplace, des flux de données brutes incluant des milliards de transactions géolocalisées issues de centaines de millions d'appareils mobiles.
* **Risques pour la vie privée :** L'absence de consentement exposait les individus à des risques accrus de harcèlement, de discrimination et de violence physique.
* **Régulation accrue :** Cette décision s'inscrit dans une campagne plus large de la FTC contre la surveillance commerciale de masse, incluant des interdictions similaires infligées à d'autres courtiers comme InMarket Media et Outlogic.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car il s'agit d'un problème de **confidentialité par conception (Privacy by Design)** et de gestion des données éthique plutôt que d'une faille logicielle technique. Le risque majeur résidait dans l'exposition volontaire de données hautement sensibles via des interfaces de données accessibles commercialement.

**Recommandations :**
* **Obtention du consentement :** Mise en place d'un mécanisme de recueil du consentement libre et éclairé (opt-in) avant toute collecte ou transfert de données de géolocalisation.
* **Programmes de conformité :** Établissement de protocoles stricts de vérification des fournisseurs pour garantir le respect du consentement à chaque étape de la chaîne de données.
* **Transparence et contrôle :** Mise à disposition d'outils permettant aux utilisateurs de connaître les tiers ayant accès à leurs données et de révoquer leur consentement.
* **Gestion du cycle de vie des données :** Définition de calendriers stricts de rétention et de suppression des données, ainsi qu'une obligation de reporting immédiat auprès de la FTC en cas d'utilisation abusive par des tiers.

---
[Source](https://www.bleepingcomputer.com/news/security/ftc-to-ban-data-broker-kochava-from-selling-americans-location-data/){:target="_blank"}
