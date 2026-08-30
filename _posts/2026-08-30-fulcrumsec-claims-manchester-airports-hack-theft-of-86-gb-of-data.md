---
title: 'FulcrumSec claims Manchester Airports hack, theft of 86 GB of data'
date: 2026-08-30
permalink: /posts/2026/08/30/fulcrumsec-claims-manchester-airports-hack-theft-of-86-gb-of-data/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données majeure au Manchester Airports Group

Le groupe d'extorsion FulcrumSec a revendiqué le vol de 86 Go de données appartenant au Manchester Airports Group (MAG), exploitant les aéroports de Manchester, Londres Stansted et East Midlands. Bien que MAG ait initialement minimisé l'incident, l'analyse d'échantillons prouve que les données exposées sont bien plus détaillées que ce qui avait été communiqué.

**Points clés :**
*   **Volume et nature des données :** Environ 86 Go de données incluant des historiques de réservations (parkings, salons, accès rapides), des identifiants clients, des informations de voyage (terminaux, dates, tarifs), ainsi que des adresses postales précises et des données de géolocalisation.
*   **Mode opératoire :** Les attaquants ont utilisé des identifiants d'API Iterable exposés dans le code JavaScript côté client.
*   **Risques :** Bien qu'aucune donnée bancaire n'ait été détectée, la précision des informations permet la création de campagnes de phishing ou d'escroqueries par téléphone (vishing) extrêmement crédibles.
*   **Impact :** Environ 8,7 millions de clients sont potentiellement touchés. Aucune perturbation opérationnelle ou compromission de la sécurité aérienne n'a été constatée.

**Vulnérabilités identifiées :**
*   **Exposition de secrets :** Identifiants d'API (Iterable) codés en dur dans des fichiers JavaScript accessibles côté client. (Pas de CVE spécifique, il s'agit d'une mauvaise pratique de développement/gestion des secrets).

**Recommandations :**
*   **Pour l'organisation :** Auditer systématiquement le code côté client pour détecter toute fuite de clés d'API ou d'identifiants sensibles. Appliquer une rotation immédiate des secrets compromis.
*   **Pour les clients :** Rester extrêmement vigilant face aux communications entrantes (e-mails, SMS, appels) concernant des réservations de voyage. Ne jamais fournir d'informations financières ou de mots de passe suite à un contact non sollicité.

---
[Source](https://www.bleepingcomputer.com/news/security/fulcrumsec-claims-manchester-airports-hack-theft-of-86-gb-of-data/){:target="_blank"}
