---
title: 'Shared secret: EDR killer in the kill chain'
date: 2025-08-06
permalink: /posts/2025/08/06/shared-secret-edr-killer-in-the-kill-chain/
tags:
- veille-cyber
- sophos
---
Voici un résumé des informations clés de l'article.

**Titre :** Escalade des Outils Désactivateurs d'EDR au Sein des Groupes de Ransomware

L'article met en évidence une tendance inquiétante : l'utilisation croissante d'outils sophistiqués conçus pour neutraliser les solutions de sécurité Endpoint Detection and Response (EDR) dans le cadre d'attaques multi-étapes. Ces "EDR killers" permettent aux acteurs malveillants d'opérer sans être détectés.

**Points Clés :**

*   **Augmentation de la Sophistication :** Depuis 2022, on observe une sophistication accrue de ces outils, souvent développés par des groupes de ransomware ou achetés sur des marchés clandestins, comme l'indiquent les fuites du groupe Black Basta.
*   **Partage d'Outils et de Connaissances :** Des preuves suggèrent un partage d'outils et de connaissances techniques entre différents groupes de ransomware concurrents (tels que RansomHub, Qilin, DragonForce, INC).
*   **Utilisation de Packers :** Les outils sont souvent obscurcis par des packers comme HeartCrypt, disponible en tant que service.
*   **Chaîne d'Attaque Typique :** Une attaque courante implique un dropper packé par HeartCrypt, qui dépose un exécutable EDR killer. Ce dernier charge ensuite un pilote signé avec un certificat compromis pour désactiver les solutions de sécurité.

**Vulnérabilités et Méthodes :**

L'outil principal décrit, nommé "AVKiller" par les chercheurs, présente plusieurs caractéristiques notables :

*   **Code Fortement Protégé :** Le code est obfusqué et protégé de manière significative.
*   **Détection de Pilote Spécifique :** Il recherche un pilote portant un nom aléatoire de cinq lettres (par exemple, `mraml.sys`).
*   **Utilisation de Certificats Compromis/Expirés :** Les pilotes utilisés sont signés par des certificats provenant d'entreprises comme Changsha Hengxiang Information Technology Co., Ltd. (révoqué depuis 2016) ou Fuzhou Dingxin Trade Co., Ltd. (expiré depuis 2012), exploitant ainsi la confiance accordée aux signatures numériques.
*   **Ciblage Étendu :** L'outil cible une large gamme de produits de sécurité, notamment Bitdefender, Cylance, F-Secure, Fortinet, Kaspersky, McAfee, Microsoft, SentinelOne, Sophos, Symantec, Trend Micro, et Webroot.
*   **Terminaison de Processus :** Il tente de terminer des processus spécifiques liés aux solutions de sécurité (par exemple, `MsMpEng.exe`, `SophosHealth.exe`, `SAVService.exe`, `sophosui.exe`).
*   **Injection dans des Outils Légitimes :** Une variante a été observée injectant du code malveillant dans `Beyond Compare`, un utilitaire légitime.
*   **Exploits Potentiels :** Dans le cas de MedusaLocker, l'infection initiale pourrait être liée à des exploits RCE zero-day dans SimpleHelp.

**Recommandations :**

L'article ne fournit pas de recommandations directes dans son corps, mais les découvertes impliquent que les organisations devraient :

*   **Maintenir les Solutions de Sécurité à Jour :** Assurer que les solutions EDR et antivirus sont correctement patchées et configurées.
*   **Surveiller les Activités Suspectes :** Porter une attention particulière aux installations de pilotes inhabituelles ou signées par des certificats douteux.
*   **Renforcer la Gestion des Certificats :** Mettre en place des contrôles pour vérifier la validité et l'origine des certificats utilisés lors de l'exécution de logiciels.
*   **Être Vigilant Face aux Packers :** Reconnaître que les techniques d'obfuscation comme celles utilisées par HeartCrypt sont courantes et peuvent dissimuler des charges utiles malveillantes.
*   **Examiner les Journaux d'Événements :** Analyser les journaux pour détecter les tentatives de terminaison de processus de sécurité ou les erreurs liées aux pilotes.

Les indicateurs de compromission (IOCs) liés à cet article sont disponibles dans le dépôt GitHub de Sophos Labs.

---
[Source](https://news.sophos.com/en-us/2025/08/06/shared-secret-edr-killer-in-the-kill-chain/){:target="_blank"}
