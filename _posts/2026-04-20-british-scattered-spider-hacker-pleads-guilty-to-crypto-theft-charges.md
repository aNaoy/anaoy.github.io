---
title: 'British Scattered Spider hacker pleads guilty to crypto theft charges'
date: 2026-04-20
permalink: /posts/2026/04/20/british-scattered-spider-hacker-pleads-guilty-to-crypto-theft-charges/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation d'un leader du collectif Scattered Spider

Tyler Robert Buchanan, un ressortissant britannique identifié comme l'un des leaders du collectif cybercriminel « Scattered Spider », a plaidé coupable aux États-Unis de fraude électronique et d'usurpation d'identité aggravée. Entre 2021 et 2023, ce groupe a infiltré au moins une douzaine d'entreprises, dérobant plus de 8 millions de dollars en cryptomonnaies via des techniques d'ingénierie sociale sophistiquées.

**Points clés :**
*   **Mode opératoire :** Utilisation massive de campagnes de SMS-phishing (smishing) imitant des services IT légitimes pour obtenir des identifiants et des données personnelles.
*   **Escalade des privilèges :** Les assaillants exploitaient les informations volées pour réaliser des attaques de type « SIM swap » (échange de carte SIM), prenant le contrôle des numéros de téléphone et des portefeuilles numériques des victimes.
*   **Impact :** Le groupe est lié à des attaques de grande envergure contre des entreprises majeures (MGM, Caesars, Twilio, Reddit, etc.) et collabore fréquemment avec des gangs de ransomware russes (BlackCat/AlphV, Qilin, RansomHub).
*   **Justice :** Buchanan risque jusqu'à 22 ans de prison, avec un verdict attendu en août 2026. Plusieurs de ses complices ont également été inculpés ou condamnés.

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; le groupe repose sur l'exploitation du **facteur humain** et des faiblesses des processus de validation d'identité.
*   **MFA Fatigue (MFA bombing) :** Bombardement de requêtes d'authentification multifacteur pour forcer l'acceptation par l'utilisateur.

**Recommandations de sécurité :**
*   **Sensibilisation :** Former les employés à la méfiance envers les messages SMS non sollicités, même s'ils semblent provenir de fournisseurs IT ou de services internes.
*   **Sécurisation du MFA :** Privilégier les méthodes d'authentification forte résistantes au phishing (clés matérielles FIDO2/WebAuthn) plutôt que les codes SMS ou les notifications push classiques.
*   **Protection contre le SIM Swapping :** Renforcer les procédures de vérification auprès des opérateurs téléphoniques et privilégier des méthodes de récupération de compte qui ne dépendent pas du numéro de téléphone mobile.
*   **Gestion des accès :** Implémenter le principe du moindre privilège pour limiter l'impact en cas de compromission d'un compte utilisateur.

---
[Source](https://www.bleepingcomputer.com/news/security/british-scattered-spider-hacker-pleads-guilty-to-crypto-theft-charges/){:target="_blank"}
