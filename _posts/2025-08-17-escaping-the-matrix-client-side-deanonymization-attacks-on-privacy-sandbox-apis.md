---
title: 'Escaping the Matrix: Client-Side Deanonymization Attacks on Privacy Sandbox APIs'
date: 2025-08-17
permalink: /posts/2025/08/17/escaping-the-matrix-client-side-deanonymization-attacks-on-privacy-sandbox-apis/
tags:
- veille-cyber
- zerodaysfans
---
## Failles dans la Confidentialité du Privacy Sandbox : Attaques de Désanonymisation Côté Client

Des faiblesses significatives ont été découvertes dans la mise en œuvre des API du Privacy Sandbox de Google, conçues pour préserver la vie privée des utilisateurs dans le cadre de la publicité en ligne. Ces vulnérabilités peuvent permettre des attaques de désanonymisation, révélant des informations sur les utilisateurs malgré les protections prévues.

### Points Clés :

*   Le Privacy Sandbox vise à remplacer les cookies tiers en offrant des alternatives pour le suivi des conversions et la segmentation d'audience.
*   Plusieurs API, notamment l'Attribution Reporting API et le Shared Storage API, ont été examinées.
*   Les attaques exploitent des fonctionnalités comme les "debug reports", les limites de stockage et le code des "worklets".

### Vulnérabilités et Exploitations :

1.  **"Debug Reports" Fuchsiques :**
    *   **Problème :** Les rapports de débogage de l'Attribution Reporting API, bien qu'utiles pour le dépannage, peuvent divulguer des informations sensibles comme le site d'origine de l'annonce, contournant les politiques de référent (comme `no-referrer`) et la Sécurité du Contenu (CSP).
    *   **Exploitation :** Cela permet aux annonceurs de savoir sur quels sites les utilisateurs voient leurs publicités, sapant ainsi la confidentialité. Par exemple, un rapport de débogage peut révéler le site éditeur principal, même lorsque l'annonce est diffusée via un `SafeFrame`.

2.  **Détournement de Destination et Oracle de Limite de Stockage :**
    *   **Problème :** L'Attribution Reporting API applique des limites de stockage pour les rapports d'événements par site de destination. Lorsque cette limite (estimée à 1000 sur Chrome) est atteinte, des rapports d'erreurs (`trigger-event-storage-limit`) sont envoyés. L'injection de destinations de débogage non existantes dans les enregistrements de sources, qui peuvent ensuite être achetées par des attaquants, permet d'exploiter cette fonctionnalité.
    *   **Exploitation :** Un attaquant peut acheter ces domaines de débogage et y enregistrer des déclencheurs. En surveillant le nombre de rapports envoyés et l'apparition des rapports d'erreurs, l'attaquant peut reconstruire l'historique de navigation de l'utilisateur, sachant quand il a visité ou non un site spécifique, et contourner les limitations de taux de rapports grâce à des enregistrements de sources sur plusieurs domaines contrôlés.

3.  **Code de Worklet Cross-Origin Non Sécurisé dans le Shared Storage API :**
    *   **Problème :** Le Shared Storage API permet de stocker des données cross-site via des "worklets". Si le code du worklet n'est pas correctement sécurisé et autorise l'usage cross-origin, des données peuvent être divulguées.
    *   **Exploitation :** Dans un exemple impliquant Criteo, un attaquant peut fournir une liste d'URLs contrôlées au worklet. En analysant quelle URL est finalement chargée dans un `fencedframe`, l'attaquant peut déduire une valeur stockée dans le Shared Storage, démontrant une fuite de données potentielle à travers les origines.

### Recommandations :

*   **Éviter les "Debug Reports" non sécurisés :** Il faut réévaluer la conception et l'implémentation des rapports de débogage pour qu'ils ne divulguent pas d'informations sensibles, en particulier sur le site d'origine de la navigation. Les politiques comme `Permissions-Policy` devraient être utilisées pour désactiver ces fonctionnalités dans les environnements sandbox (comme vu avec Facebook).
*   **Auditer et sécuriser les destinations de débogage :** Les plateformes publicitaires doivent cesser d'injecter des destinations de débogage non existantes. Une meilleure gestion des limites de stockage et l'absence de fuites d'information via les rapports d'erreurs sont nécessaires.
*   **Sécuriser le code des Worklets :** Les développeurs du Shared Storage API doivent s'assurer que le code des worklets est correctement isolé et qu'il n'y a pas de fuites d'informations sensibles à travers les mécanismes d'output gates ou les appels cross-origin.
*   **Recherche continue :** La complexité des nouvelles API du Privacy Sandbox nécessite une scrutiny accrue par les chercheurs en sécurité et en confidentialité afin d'identifier et de corriger les vulnérabilités avant qu'elles ne soient exploitées à grande échelle.

---
[Source](https://spaceraccoon.dev/client-side-deanonymization-attacks-privacy-sandbox-apis/){:target="_blank"}
