---
title: 'Shared secret: EDR killer in the kill chain'
date: 2025-08-07
permalink: /posts/2025/08/07/shared-secret-edr-killer-in-the-kill-chain/
tags:
- veille-cyber
- sophos
---
### Évolution des Outils de Désactivation des Solutions de Sécurité Endpoint

Un nombre croissant de groupes de ransomware développent ou acquièrent des outils sophistiqués pour neutraliser les solutions de sécurité Endpoint (EDR), une étape cruciale dans les attaques multi-étapes pour opérer sans être détectés. Ces outils, souvent obscurcis par des packers comme HeartCrypt, ciblent spécifiquement les processus et services des produits antivirus et EDR.

**Points Clés :**

*   **Objectif :** Désactiver les solutions EDR et antivirus pour permettre aux attaquants d'agir discrètement.
*   **Source :** Développés par des groupes de ransomware ou achetés sur des marchés clandestins, comme le suggèrent les fuites du groupe Black Basta.
*   **Technique Principale :** Utilisation d'un exécutable malveillant qui charge un pilote système (driver) signé avec des certificats compromis ou révoqués.
*   **Obsfuscation :** Les outils sont souvent packés (par exemple, avec HeartCrypt) pour échapper à la détection.
*   **Partage de Techniques :** Des preuves suggèrent un partage de code et de connaissances entre différents groupes de ransomware (RansomHub, Qilin, DragonForce, INC, etc.), utilisant des variantes similaires du même outil.

**Vulnérabilités et Techniques d'Attaque :**

*   **EDRKillShifter :** Créé par le groupe RansomHub, un prédécesseur de l'outil décrit.
*   **AVKiller (Exemple d'Outil) :**
    *   **Mécanisme :** S'insère dans des utilitaires légitimes (comme Beyond Compare) pour masquer son activité. Le code malveillant est injecté en tant que ressource et décodé à l'exécution.
    *   **Caractéristiques Notables :** Code fortement protégé, recherche d'un pilote avec un nom aléatoire (par exemple, `mraml.sys`), utilisation de certificats compromis (par exemple, de "Changsha Hengxiang Information Technology Co., Ltd." révoqué depuis 2016, ou de "Fuzhou Dingxin Trade Co., Ltd." révoqué depuis 2012).
    *   **Ciblage :** Vise une large gamme de produits de sécurité, notamment Bitdefender, Cylance, Eset, F-Secure, Fortinet, HitManPro, Kaspersky, McAfee, Microsoft, SentinelOne, Sophos, Symantec, Trend Micro, Webroot.
    *   **Processus Ciblés :** Tente de terminer des processus comme `MsMpEng.exe`, `SophosHealth.exe`, `SAVService.exe`, `sophosui.exe`.
*   **Attaques Multi-étapes :** L'outil AVKiller est souvent observé en conjonction avec des campagnes de ransomware (RansomHub, Blacksuit, Medusa, Qilin, DragonForce, Crytox, Lynx, INC).
*   **Exploitation de Vulnérabilités :** Dans certains cas, comme avec MedusaLocker, l'outil a été déployé via une vulnérabilité "zero-day" dans des logiciels de support à distance (par exemple, SimpleHelp).

**Recommandations :**

*   **Surveillance Active :** Maintenir une vigilance constante sur les comportements suspects, tels que l'installation de services inhabituels ou la présence de pilotes système inconnus.
*   **Mises à Jour :** Assurer que tous les logiciels, y compris les solutions de sécurité et les utilitaires système, sont maintenus à jour pour corriger les vulnérabilités connues.
*   **Gestion des Certificats :** Surveiller l'utilisation de certificats compromis ou révoqués pour la signature de pilotes.
*   **Solutions de Sécurité à Jour :** Utiliser des solutions de sécurité Endpoint avec des protections dynamiques (comme SysCall, DynamicShellcode, HollowProcess) et des détections statiques génériques robustes.
*   **Analyse des Packers :** Disposer de capacités d'analyse capables de contourner les techniques d'obfuscation avancées.

---
[Source](https://news.sophos.com/en-us/2025/08/06/shared-secret-edr-killer-in-the-kill-chain/){:target="_blank"}
