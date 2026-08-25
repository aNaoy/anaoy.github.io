---
title: 'Hackers target WordPress sites in miniOrange auth bypass attacks'
date: 2026-08-25
permalink: /posts/2026/08/25/hackers-target-wordpress-sites-in-miniorange-auth-bypass-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par contournement d'authentification sur le plugin miniOrange SAML SSO

Des pirates exploitent activement deux vulnérabilités critiques dans le plugin WordPress **miniOrange SAML 2.0 Single Sign On**. En enchaînant ces failles, des attaquants peuvent forger des réponses SAML et usurper l'identité d'un administrateur pour prendre le contrôle total des sites vulnérables.

**Points clés :**
*   **Mécanisme d'attaque :** Les attaquants manipulent l'algorithme de signature pour forcer la validation d'une clé publique comme clé partagée (HMAC-SHA1) et exploitent une erreur de vérification OpenSSL pour valider des signatures malveillantes.
*   **État de la menace :** Des tentatives d'exploitation réelles ont été détectées. Une preuve de concept (PoC) est disponible publiquement, augmentant les risques d'attaques à grande échelle.
*   **Risque lié aux versions payantes :** L'éditeur a communiqué de manière incomplète sur la correction des versions payantes, laissant de nombreux administrateurs sans alerte de mise à jour.

**Vulnérabilités :**
*   **CVE-2026-61979 :** Permet de contourner la vérification de signature en forçant l'utilisation d'un algorithme HMAC-SHA1 avec une clé publique connue.
*   **CVE-2026-15981 :** Traite à tort une erreur de vérification OpenSSL comme un succès, permettant aux signatures falsifiées de passer outre la sécurité.

**Recommandations :**
*   **Mise à jour immédiate :** Les propriétaires de sites doivent mettre à jour manuellement leur plugin vers les versions corrigées listées ci-dessous, car les notifications automatiques peuvent être défaillantes pour les versions payantes :
    *   **Free :** 5.4.5
    *   **Premium (Single) :** 13.0.4
    *   **Standard (Single) :** 17.06
    *   **Premium/Enterprise/All-Inclusive (Multisite) :** 20.2.8
    *   **Enterprise/All-Inclusive (Single) :** 26.0.3
    *   **VIP (Single) :** 32.0.8
    *   **VIP (Multisite) :** 35.0.7
*   **Vérification manuelle :** Puisque le tableau de bord WordPress n'affiche pas toujours les alertes pour les éditions payantes, une vérification manuelle de la version installée est impérative.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-wordpress-sites-in-miniorange-auth-bypass-attacks/){:target="_blank"}
