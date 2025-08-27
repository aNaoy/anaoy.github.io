---
title: 'Blind Eagle’s Five Clusters Target Colombia Using RATs, Phishing Lures, and Dynamic DNS Infra'
date: 2025-08-27
permalink: /posts/2025/08/27/blind-eagles-five-clusters-target-colombia-using-rats-phishing-lures-and-dynamic-dns-infra/
tags:
- veille-cyber
- hackernews
---
**Blind Eagle : Ciblage persistant de la Colombie**

Entre mai 2024 et juillet 2025, l'acteur de menace connu sous le nom de Blind Eagle, également suivi sous le nom de TAG-144, a ciblé de manière significative la Colombie, avec des incursions en Équateur, au Chili, au Panama et auprès d'utilisateurs hispanophones en Amérique du Nord. Les attaques visent principalement les entités gouvernementales colombiennes à tous les niveaux, mais touchent également les secteurs de la finance, de l'éducation, de la santé, de l'énergie, du pétrole, de la fabrication et des services professionnels. Les motivations semblent être un mélange d'espionnage cybernétique et de gains financiers.

**Points Clés :**

*   **Cinq grappes d'activités distinctes** ont été identifiées, utilisant des tactiques, techniques et procédures (TTP) similaires mais avec des infrastructures et des méthodes de déploiement de logiciels malveillants différentes.
*   L'acteur de menace s'appuie sur des **chevaux de Troie d'accès à distance (RAT) open source ou crackés**, notamment Lime RAT, DCRat, AsyncRAT et Remcos RAT.
*   L'infrastructure de commande et de contrôle (C2) utilise des **services DNS dynamiques** (duckdns.org, ip-ddns.com, noip.com) et des **serveurs privés virtuels (VPS)**, ainsi que des services Internet légitimes (LIS) comme Bitbucket, Discord, GitHub, Google Drive pour masquer le contenu malveillant.
*   Les campagnes utilisent souvent des **appâts d'hameçonnage ciblé** (spear-phishing) se faisant passer pour des agences gouvernementales locales, avec des documents malveillants ou des liens raccourcis.
*   Un recours à des **scripts Visual Basic et PowerShell** est observé pour exécuter des charges utiles et télécharger des modules d'injection.
*   Une **version crackée d'AsyncRAT** a été précédemment associée à d'autres groupes de menace ciblant la Colombie.
*   Environ **60% des activités observées ont ciblé le secteur gouvernemental**.

**Vulnérabilités :**

*   Bien qu'aucun numéro CVE spécifique ne soit mentionné dans l'article, les attaques exploitent des vulnérabilités associées à la **livraison de malware via des documents malveillants** et des **composants de RAT** potentiellement obsolètes ou mal sécurisés dans les versions crackées.

**Recommandations :**

*   **Renforcer la sensibilisation et la formation des employés** aux techniques d'hameçonnage, à la prudence face aux documents et liens suspects, en particulier ceux provenant d'agences gouvernementales.
*   **Surveiller et sécuriser l'infrastructure de réseau**, y compris les VPN, les VPS et les services DNS, pour détecter toute activité suspecte ou non autorisée.
*   **Mettre en place des solutions de sécurité robustes** capables de détecter et de bloquer les RAT et les scripts malveillants.
*   **Exécuter des analyses régulières des systèmes** pour identifier et supprimer les logiciels malveillants.
*   **Limiter l'utilisation et la confiance accordée aux services Internet légitimes** à des fins de stockage ou de distribution de fichiers sensibles si l'activité de l'attaquant y est détectée.

---
[Source](https://thehackernews.com/2025/08/blind-eagles-five-clusters-target.html){:target="_blank"}
