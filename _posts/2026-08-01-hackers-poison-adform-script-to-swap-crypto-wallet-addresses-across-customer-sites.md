---
title: 'Hackers Poison Adform Script to Swap Crypto Wallet Addresses Across Customer Sites'
date: 2026-08-01
permalink: /posts/2026/08/01/hackers-poison-adform-script-to-swap-crypto-wallet-addresses-across-customer-sites/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement Adform : détournement d'adresses crypto

L'entreprise de technologie publicitaire Adform a été victime d'une attaque par chaîne d'approvisionnement visant son script JavaScript `trackpoint-async.js`. Des attaquants ont injecté un code malveillant dans ce fichier, largement diffusé sur de nombreux sites clients, afin de substituer les adresses de portefeuilles de cryptomonnaies (Bitcoin, Ethereum, Tron) par celles des attaquants lors de transactions effectuées par les utilisateurs.

**Points clés :**
*   **Méthodologie :** Le script malveillant surveillait le presse-papier, les événements de saisie et les formulaires web pour remplacer en temps réel les adresses crypto.
*   **Persistence :** Le code ne s'installait pas sur les machines, mais s'exécutait tant qu'une page compromise restait ouverte.
*   **Portée :** En raison de la nature partagée du script, l'attaque a touché une multitude de sites tiers sans nécessiter de compromission individuelle de chacun d'eux.
*   **Étendue incertaine :** Bien qu'Adform ait identifié l'incident au 27 juillet, des chercheurs suggèrent que l'activité malveillante aurait pu durer plus longtemps.

**Vulnérabilités :**
*   **Type :** Compromission de la chaîne d'approvisionnement (Supply Chain Attack) via l'injection de code dans une ressource JavaScript tierce.
*   **CVE :** Aucune CVE n'a été attribuée à ce jour, l'incident relevant d'une attaque applicative spécifique au fournisseur.

**Recommandations :**
*   **Utilisateurs :** Vider systématiquement le cache de son navigateur pour s'assurer que le fichier JavaScript corrompu est supprimé.
*   **Vigilance :** Vérifier minutieusement toute adresse de portefeuille avant de valider une transaction.
*   **Clients d'Adform :** Mettre en œuvre des mesures de sécurité pour les ressources tierces, comme l'utilisation de la sous-intégrité des ressources (Subresource Integrity - SRI) afin de détecter toute modification non autorisée des scripts chargés.

---
[Source](https://thehackernews.com/2026/08/hackers-poison-adform-script-to-swap.html){:target="_blank"}
