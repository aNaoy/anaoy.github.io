---
title: 'Online retailer PcComponentes says data breach claims are fake'
date: 2026-01-22
permalink: /posts/2026/01/22/online-retailer-pccomponentes-says-data-breach-claims-are-fake/
tags:
- veille-cyber
- bleepingcomp
---
## Retailer PcComponentes Confronts Credential Stuffing Attack

La société espagnole PcComponentes, un important détaillant technologique, a fermement démenti les allégations d'une violation de données massive affectant 16 millions de clients. Bien qu'un acteur malveillant ait prétendu avoir volé et mis en vente une base de données client, l'entreprise affirme qu'il n'y a eu aucun accès illégitime à ses bases de données ou systèmes internes. Elle a également souligné que le chiffre de 16 millions de clients prétendument affectés est inexact, le nombre de comptes actifs étant considérablement inférieur. De plus, aucune information financière ou mot de passe client n'est stocké sur leurs systèmes.

Cependant, PcComponentes a reconnu avoir subi une attaque par "credential stuffing". Cette technique consiste pour des acteurs malveillants à utiliser des identifiants (adresses e-mail et mots de passe) provenant d'autres violations de données ou de fuites pour tenter de s'introduire sur des comptes d'autres services. Une analyse a révélé que les données d'identification utilisées dans cette attaque provenaient très probablement d'ordinateurs infectés par des logiciels malveillants voleurs d'informations.

Pour un nombre limité de comptes compromis par cette attaque, les données exposées incluent :
* Noms et prénoms
* Numéro d'identification national
* Adresses physiques
* Adresses IP
* Adresses e-mail
* Numéros de téléphone

En réponse à cet incident, PcComponentes a renforcé ses défenses. Les mesures mises en place incluent l'ajout de CAPTCHAs sur les pages de connexion, la nouvelle activation obligatoire de l'authentification à deux facteurs (2FA) pour tous les comptes, et l'invalidation de toutes les sessions actives. Les clients seront automatiquement déconnectés et devront activer la 2FA pour retrouver l'accès à leur compte.

### Points clés :

*   **Nature de l'incident :** Le site a été victime d'une attaque par "credential stuffing", et non d'une fuite de données directe de ses propres systèmes.
*   **Données compromises (pour un petit nombre de comptes) :** Noms, identifiants nationaux, adresses physiques, adresses IP, e-mails, numéros de téléphone.
*   **Absence de données sensibles :** Les mots de passe et les informations financières ne sont pas stockés par l'entreprise.
*   **Origine des identifiants :** Proviennent probablement de logiciels malveillants voleurs d'informations et d'autres violations de données.

### Vulnérabilités :

*   L'article ne mentionne pas de CVE spécifiques, mais l'attaque exploite la réutilisation de mots de passe entre différents services, une faiblesse générale des utilisateurs.

### Recommandations :

*   **Pour PcComponentes :**
    * Implémentation de CAPTCHAs sur les pages de connexion.
    * Activation obligatoire de l'authentification à deux facteurs (2FA) pour tous les comptes.
    * Invalidation de toutes les sessions actives pour forcer une nouvelle authentification sécurisée.
*   **Pour les clients (recommandations générales de l'entreprise) :**
    * Utiliser des mots de passe forts et uniques pour chaque compte.
    * Stocker les mots de passe dans un gestionnaire de mots de passe.
    * Rester vigilant face aux potentiels messages de phishing.

---
[Source](https://www.bleepingcomputer.com/news/security/online-retailer-pccomponentes-says-data-breach-claims-are-fake/){:target="_blank"}
