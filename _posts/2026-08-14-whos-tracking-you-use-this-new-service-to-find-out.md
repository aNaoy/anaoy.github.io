---
title: 'Who’s Tracking You? Use This New Service to Find Out'
date: 2026-08-14
permalink: /posts/2026/08/14/whos-tracking-you-use-this-new-service-to-find-out/
tags:
- veille-cyber
- krebs
---
### Transparence publicitaire : Démasquer les traqueurs avec DecryptAds

Le service en ligne **DecryptAds** a été lancé pour apporter de la transparence dans l'écosystème opaque de la publicité numérique (adtech). En analysant et en corrélant les données publiques (`ads.txt`, `app-ads.txt`, `sellers.json`), cet outil permet d'identifier précisément les entreprises qui collectent des données ou diffusent des publicités sur un site web ou une application mobile.

**Points clés :**
*   **Analyse de la chaîne d'approvisionnement :** DecryptAds met en évidence des relations complexes entre les éditeurs et les courtiers en données, révélant parfois des conflits d'intérêts où une régie publicitaire joue à la fois le rôle d'acheteur et de vendeur.
*   **Risques géopolitiques :** Le service identifie les partenaires publicitaires basés dans des pays à haut risque (Russie, Chine, Émirats arabes unis), permettant de repérer des entités sous sanctions internationales intégrées dans les chaînes de publicité de sites sensibles (médias militaires, sites d'actualité).
*   **Détection des fraudes et « AI Slop » :** L'outil permet de traquer les réseaux de sites générés par IA, souvent utilisés pour diffuser des logiciels malveillants (*malvertising*) ou usurper l'identité de terminaux (ex: détournement d'appareils de streaming TV).
*   **Suivi des « suppressions silencieuses » :** Une fonctionnalité recense les partenaires publicitaires soudainement retirés des fichiers de déclaration des plateformes, un signe fréquent d'activités frauduleuses cachées au public.

**Vulnérabilités :**
*   **Absence de transparence sur le SCO (Supply Chain Object) :** La non-divulgation des données de transactions côté serveur empêche les victimes de malvertising d'identifier précisément l'origine d'une charge utile malveillante (*zero-click*).
*   **Failles dans la chaîne publicitaire :** La prolifération de sites de faible qualité (« AI slop ») sert de vecteur pour des campagnes de phishing et de malwares.

**Recommandations :**
*   **Bloquer les publicités :** L'utilisation de bloqueurs de publicités est la méthode la plus efficace pour limiter le pistage.
    *   *PC/Ordinateurs :* **uBlock Origin Lite** (extension).
    *   *Réseau domestique :* Installation d'un **Pi-hole** sur un Raspberry Pi pour un filtrage DNS au niveau du routeur.
*   **Prudence avec les applications mobiles :** Privilégiez l'accès aux services via un navigateur web plutôt que via des applications dédiées, ces dernières collectant généralement beaucoup plus de données privées et de métadonnées de géolocalisation.
*   **Audit de sécurité :** Les organisations doivent utiliser les outils comme DecryptAds pour auditer leurs propres partenaires publicitaires et s'assurer qu'aucun acteur à risque n'est présent dans leur chaîne d'approvisionnement numérique.

---
[Source](https://krebsonsecurity.com/2026/08/whos-tracking-you-use-this-new-service-to-find-out/){:target="_blank"}
