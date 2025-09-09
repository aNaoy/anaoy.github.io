---
title: '20 Popular npm Packages With 2 Billion Weekly Downloads Compromised in Supply Chain Attack'
date: 2025-09-09
permalink: /posts/2025/09/09/20-popular-npm-packages-with-2-billion-weekly-downloads-compromised-in-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
**Attaque sur la chaîne d'approvisionnement logicielle npm : des paquets populaires compromis**

Une attaque de la chaîne d'approvisionnement logicielle a affecté plus de 20 paquets npm populaires, utilisés collectivement plus de 2 milliards de fois par semaine. L'incident a débuté lorsqu'un mainteneur de paquets a été victime d'une attaque de phishing, lui faisant divulguer ses identifiants d'authentification multifacteur. Ces informations volées ont permis aux attaquants de publier des versions malveillantes de paquets sur le registre npm.

**Points clés :**

*   **Méthode d'attaque :** Le mainteneur a été ciblé par un e-mail frauduleux prétendant provenir de npm, l'incitant à mettre à jour ses informations d'authentification multifacteur. La page de phishing a servi à capturer le nom d'utilisateur, le mot de passe et le jeton 2FA, probablement via une attaque "adversary-in-the-middle" (AitM).
*   **Malware :** Le code malveillant injecté dans les paquets compromis est conçu pour intercepter les transactions de cryptomonnaies. Il remplace l'adresse du portefeuille de destination par une adresse contrôlée par l'attaquant, en utilisant la distance de Levenshtein pour trouver des correspondances proches.
*   **Ciblage :** Le malware agit comme un intercepteur basé sur le navigateur, détournant le trafic réseau et les API d'application (tels que `window.fetch`, `XMLHttpRequest`, `window.ethereum.request`) pour voler des actifs en cryptomonnaies. Les utilisateurs finaux qui visitent des sites utilisant ces paquets compromis et qui ont des portefeuilles connectés sont directement ciblés. Les développeurs peuvent également être affectés s'ils ouvrent un site concerné avec un portefeuille connecté.
*   **Portée étendue :** L'attaque s'est étendue à un autre mainteneur de haut profil, "duckdb\_admin", utilisant le même malware pour distribuer le code malveillant.

**Vulnérabilités exploitées :**

*   Compromission d'un compte mainteneur via une attaque de phishing.
*   Utilisation des identifiants compromis pour publier du code malveillant dans des paquets légitimes.

**Recommandations :**

*   **Vigilance accrue :** Les développeurs doivent faire preuve d'une vigilance constante concernant les e-mails et les demandes de mise à jour d'informations sensibles.
*   **Sécurisation des chaînes CI/CD :** Renforcer la sécurité des pipelines d'intégration et de déploiement continus (CI/CD).
*   **Verrouillage des dépendances :** Gérer et verrouiller rigoureusement les dépendances utilisées dans les projets.
*   **Audit régulier des paquets :** Examiner régulièrement les paquets dont on dépend, surtout ceux provenant de sources externes ou ayant des mainteneurs moins connus.
*   **Utilisation d'outils de sécurité :** Examiner l'utilisation d'outils d'analyse de sécurité de la chaîne d'approvisionnement pour détecter les comportements suspects.

**Paquets affectés initialement (liste non exhaustive) :**

*   ansi-regex@6.2.1
*   ansi-styles@6.2.2
*   backslash@0.2.1
*   chalk@5.6.1
*   chalk-template@1.1.1
*   color-convert@3.1.1
*   color-name@2.0.1
*   color-string@2.1.1
*   debug@4.4.2
*   error-ex@1.3.3
*   has-ansi@6.0.1
*   is-arrayish@0.3.3
*   proto-tinker-wc@1.8.7
*   supports-hyperlinks@4.1.1
*   simple-swizzle@0.2.3
*   slice-ansi@7.1.1
*   strip-ansi@7.1.1
*   supports-color@10.2.1
*   supports-hyperlinks@4.1.1
*   wrap-ansi@9.0.1

**Paquets supplémentaires affectés par la propagation du malware :**

*   @coveops/abi@2.0.1
*   @duckdb/duckdb-wasm@1.29.2
*   @duckdb/node-api@1.3.3
*   @duckdb/node-bindings@1.3.3
*   duckdb@1.3.3
*   prebid@10.9.1
*   prebid@10.9.2
*   prebid-universal-creative@1.17.3

---
[Source](https://thehackernews.com/2025/09/20-popular-npm-packages-with-2-billion.html){:target="_blank"}
