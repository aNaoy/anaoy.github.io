---
title: 'Nordstroms email system abused to send crypto scams to customers'
date: 2026-03-19
permalink: /posts/2026/03/19/nordstroms-email-system-abused-to-send-crypto-scams-to-customers/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission du système d'email de Nordstrom pour une escroquerie aux cryptomonnaies

Des pirates ont compromis le système d'envoi d'emails de l'enseigne Nordstrom pour diffuser une escroquerie aux cryptomonnaies sous couvert d'une promotion pour la Saint-Patrick. Les messages, envoyés depuis l'adresse officielle de l'entreprise, promettaient de doubler tout dépôt en cryptomonnaies effectué par les clients, créant un sentiment d'urgence avec un délai de deux heures.

**Points clés :**
*   **Vecteur d'attaque :** La compromission a été rendue possible via une attaque sur le système d'authentification unique (SSO) Okta, liée à Salesforce, permettant aux attaquants d'accéder à *Salesforce Marketing Cloud*.
*   **Impact :** Bien que l'étendue totale de la campagne soit inconnue, des clients ont été dupés et les attaquants ont récolté plus de 5 600 $.
*   **Indicateurs de fraude :** Malgré l'adresse légitime, le message contenait des erreurs de frappe (ex: "Normstorm") et un contenu illégitime invitant à des transactions financières par cryptomonnaies.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, mais l'incident souligne une faille dans la chaîne d'approvisionnement des accès tiers (Okta SSO vers Salesforce), illustrant une tendance croissante d'attaques similaires ciblant d'autres entreprises comme Betterment et GrubHub.

**Recommandations :**
*   **Pour les utilisateurs :** Ne jamais transférer de fonds ou de données sensibles suite à une sollicitation par email, même provenant d'une source officielle. Toujours vérifier les promotions directement sur le site web ou les canaux officiels de l'enseigne.
*   **Pour les entreprises :** Renforcer la sécurité des accès SSO, mettre en œuvre une authentification multi-facteurs (MFA) robuste et surveiller étroitement les accès aux plateformes tierces de marketing ou de gestion de la relation client.

---
[Source](https://www.bleepingcomputer.com/news/security/nordstroms-email-system-abused-to-send-crypto-scams-to-customers/){:target="_blank"}
