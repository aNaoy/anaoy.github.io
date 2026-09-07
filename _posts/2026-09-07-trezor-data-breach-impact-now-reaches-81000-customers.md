---
title: 'Trezor data breach impact now reaches 81,000 customers'
date: 2026-09-07
permalink: /posts/2026/09/07/trezor-data-breach-impact-now-reaches-81000-customers/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez Trezor : 81 000 clients exposés via un prestataire

Une fuite de données chez le prestataire logistique ShipMonk a compromis les informations personnelles de 81 000 clients de Trezor. Initialement estimée à 14 000 personnes, l'exposition s'est étendue après la découverte que le prestataire n'avait pas supprimé les données des commandes passées entre 2019 et 2021, malgré ses engagements contractuels. Les systèmes internes de Trezor restent sécurisés, mais les données clients (noms, adresses, emails, numéros de téléphone) sont désormais entre les mains de tiers malveillants.

**Points clés :**
* **Étendue :** 81 000 clients affectés au total (USA et divers pays européens/sud-américains).
* **Cause :** Non-respect par le prestataire ShipMonk de la politique de suppression des données.
* **Auteurs présumés :** Le groupe d'extorsion "ShinyHunters".
* **Contexte :** Cette faille s'inscrit dans une campagne plus large ciblant la plateforme d'analyse Metabase.

**Vulnérabilité :**
* Exploitation d'une faille critique de type **SQL Injection** (Zero-day) dans la plateforme Metabase, permettant aux attaquants d'obtenir des accès administrateur sur les instances des clients de l'outil.

**Recommandations :**
* **Vigilance accrue :** Les clients concernés doivent se méfier de toute communication non sollicitée (emails, appels, courriers) demandant des informations personnelles ou des identifiants.
* **Protection contre le phishing :** Risque élevé de tentatives de vol des phrases de récupération (seed phrases) de portefeuilles, une méthode déjà observée lors d'incidents précédents chez Trezor.
* **Sécurité tiers :** L'incident souligne l'importance pour les entreprises d'auditer réellement la gestion du cycle de vie des données par leurs prestataires tiers, plutôt que de se fier uniquement aux assurances écrites.

---
[Source](https://www.bleepingcomputer.com/news/security/trezor-data-breach-impact-now-reaches-81-000-customers/){:target="_blank"}
