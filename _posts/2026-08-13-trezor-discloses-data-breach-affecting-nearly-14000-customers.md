---
title: 'Trezor discloses data breach affecting nearly 14,000 customers'
date: 2026-08-13
permalink: /posts/2026/08/13/trezor-discloses-data-breach-affecting-nearly-14000-customers/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez Trezor via un prestataire logistique

Le fabricant de portefeuilles matériels Trezor a subi une fuite de données affectant près de 14 000 clients, suite au piratage de son prestataire logistique, ShipMonk. Bien que les systèmes internes de Trezor restent sécurisés, les données personnelles de clients situés dans plusieurs pays (incluant les États-Unis, le Royaume-Uni et divers pays d'Europe) ont été compromises.

**Points clés :**
* **Impact :** 13 689 clients touchés (11 742 avec une exposition complète et 1 947 avec une exposition partielle).
* **Données compromises :** Noms complets, adresses de livraison, adresses e-mail et numéros de téléphone.
* **Origine :** Une faille de sécurité exploitée sur la plateforme d'analyse tierce **Metabase**, utilisée par le prestataire ShipMonk.
* **Contexte :** Les attaquants auraient cherché à extorquer le prestataire. Ce type de vulnérabilité a également touché d'autres entreprises comme Framework et Tally.

**Vulnérabilité :**
* Une vulnérabilité **zero-day d'injection SQL** critique dans le logiciel Metabase, permettant aux attaquants d'obtenir des privilèges d'administrateur et d'exfiltrer des données.

**Recommandations pour les utilisateurs :**
* **Vigilance accrue :** Soyez extrêmement prudent face aux e-mails, appels ou messages non sollicités, car les données volées seront probablement utilisées pour des campagnes de phishing sophistiquées.
* **Protection des actifs :** Ne partagez jamais votre phrase de récupération (seed phrase) de 24 mots, même si une communication semble provenir officiellement de Trezor.
* **Authentification :** En cas de doute sur une communication reçue, contactez directement le support officiel via les canaux sécurisés de Trezor et ne cliquez jamais sur les liens contenus dans les messages suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/trezor-discloses-data-breach-affecting-nearly-14-000-customers/){:target="_blank"}
