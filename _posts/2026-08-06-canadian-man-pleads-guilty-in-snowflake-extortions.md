---
title: 'Canadian Man Pleads Guilty in Snowflake Extortions'
date: 2026-08-06
permalink: /posts/2026/08/06/canadian-man-pleads-guilty-in-snowflake-extortions/
tags:
- veille-cyber
- krebs
---
### Condamnation d'un acteur majeur dans l'affaire d'extorsion Snowflake

Connor Riley Moucka, un citoyen canadien de 26 ans, a plaidé coupable de fraude informatique et de complot après avoir orchestré une campagne massive d'extorsion visant plus de 165 entreprises clientes de la plateforme de stockage cloud **Snowflake**. Entre février et octobre 2024, lui et ses complices ont dérobé des téraoctets de données sensibles, incluant des informations financières, des dossiers de paie, ainsi que des historiques d'appels et de SMS de millions de clients AT&T.

**Points clés :**
* **Modus operandi :** Utilisation d'identifiants volés pour accéder aux comptes Snowflake.
* **Victimes notables :** TicketMaster, Lending Tree, Advance Auto Parts, Neiman Marcus et des millions d'abonnés AT&T.
* **Extorsion réitérée :** Les attaquants menaçaient de publier les données volées pour obtenir des rançons (plus de 2,5 millions de dollars récoltés). Ils ont même tenté de ré-extorquer des victimes en ciblant des fonctionnaires et leurs familles.
* **Complexité du réseau :** Implication de co-conspirateurs, notamment Cameron Wagenius (soldat américain) et John Erin Binns (impliqué dans le piratage de T-Mobile en 2021).

**Vulnérabilités exploitées :**
* Absence de **Multi-Factor Authentication (MFA)** : La faille principale a été l'utilisation de comptes clients Snowflake ne sécurisant pas leurs accès par une authentification à plusieurs facteurs.
* Gestion des identifiants : Usage de mots de passe compromis issus de fuites antérieures pour infiltrer des systèmes cloud mal sécurisés.

**Recommandations :**
* **Généralisation du MFA :** Imposer systématiquement l'authentification multifacteur pour tous les accès aux services cloud.
* **Renforcement des politiques de mots de passe :** Augmenter la complexité requise pour les identifiants afin de limiter les attaques par force brute ou usage d'identifiants volés.
* **Surveillance proactive :** Les organisations doivent surveiller les accès inhabituels aux environnements cloud pour détecter rapidement les exfiltrations de données massives.

---
[Source](https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/){:target="_blank"}
