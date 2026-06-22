---
title: '29-Year-Old Squid Proxy Bug Squidbleed Can Leak Cleartext HTTP Requests'
date: 2026-06-22
permalink: /posts/2026/06/22/29-year-old-squid-proxy-bug-squidbleed-can-leak-cleartext-http-requests/
tags:
- veille-cyber
- hackernews
---
### Squidbleed : Une vulnérabilité historique expose le trafic proxy

Une faille de sécurité majeure, baptisée **Squidbleed**, a été découverte dans le proxy web Squid. Présente depuis 1997 dans le code de parsing FTP, cette vulnérabilité permet à un utilisateur authentifié d'un réseau partagé (entreprise, école, Wi-Fi public) de voler des données sensibles transitant via le proxy.

**Points clés :**
*   **Mécanisme :** La vulnérabilité est un dépassement de lecture mémoire (*heap over-read*). Le parser FTP ne gère pas correctement les fins de chaînes de caractères, ce qui permet à un attaquant de lire des zones mémoire récemment libérées.
*   **Impact :** L'attaquant peut récupérer des requêtes HTTP en clair, incluant des jetons de session et des identifiants de connexion appartenant à d'autres utilisateurs du même proxy.
*   **Conditions d'exploitation :** L'attaquant doit avoir accès au proxy et forcer la victime à interagir avec un serveur FTP contrôlé par l'attaquant sur le port 21.

**Vulnérabilité identifiée :**
*   **CVE-2026-47729** (Score CVSS : 6.5 - Risque modéré)

**Recommandations :**
*   **Désactiver FTP :** La mesure la plus efficace consiste à désactiver totalement la prise en charge du protocole FTP dans Squid, celui-ci étant devenu obsolète pour la majorité des usages modernes.
*   **Mise à jour :** Appliquer les correctifs officiels. Bien que le suivi des versions puisse être confus (correctifs intégrés à partir de la version 7.6/7.7), il est crucial de vérifier la présence du correctif spécifique dans le fichier `FtpGateway.cc` ou de s'assurer que la distribution Linux utilisée a bien backporté la correction.
*   **Vérification :** Ne pas se fier uniquement au numéro de version, mais confirmer la correction du code source ou la mise à jour effective via les dépôts de confiance.

---
[Source](https://thehackernews.com/2026/06/29-year-old-squid-proxy-bug-squidbleed.html){:target="_blank"}
