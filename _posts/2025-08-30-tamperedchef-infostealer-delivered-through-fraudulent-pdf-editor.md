---
title: 'TamperedChef infostealer delivered through fraudulent PDF Editor'
date: 2025-08-30
permalink: /posts/2025/08/30/tamperedchef-infostealer-delivered-through-fraudulent-pdf-editor/
tags:
- veille-cyber
- bleepingcomp
---
### App Gratuite pour PDF : Porte d'Entrée d'un Voleur d'Informations

Une campagne de distribution de malwares utilise des sites web promus via Google Ads pour proposer une fausse application d'édition de PDF. Une fois installée, cette application, nommée AppSuite PDF Editor, peut activer un logiciel espion connu sous le nom de TamperedChef. Cette opération complexe implique plusieurs applications qui peuvent s'enchaîner, certaines incitant les utilisateurs à transformer leur appareil en proxy résidentiel. Plus de 50 domaines ont été identifiés, distribuant des applications signées avec de faux certificats émis par au moins quatre sociétés.

Les chercheurs estiment que les opérateurs ont délibérément attendu la fin des campagnes publicitaires pour activer les fonctions malveillantes des applications. Le malware TamperedChef, une fois mis à jour via un argument spécifique, recherche les agents de sécurité et accède aux données sensibles des navigateurs web en exploitant l'API DPAPI de Windows.

Cette initiative s'inscrit dans une opération plus large ayant débuté en juin, avec des versions du malware apparues sur VirusTotal dès mai. En plus de voler des informations, certaines applications comme OneStart, qui peut télécharger AppSuite-PDF, transforment les appareils en proxies résidentiels, potentiellement pour des activités illicites. Bien que certains certificats aient été révoqués, le risque persiste pour les installations existantes. Les chercheurs soulignent que même si ces programmes sont souvent classés comme potentiellement indésirables, leurs fonctionnalités s'apparentent à celles de malwares.

**Points Clés :**
*   Distribution d'un logiciel espion (TamperedChef) via une fausse application d'édition de PDF (AppSuite PDF Editor).
*   Utilisation de publicités Google pour attirer les victimes.
*   Activation retardée des fonctions malveillantes après la phase de promotion.
*   Vol d'informations sensibles (identifiants, cookies) à l'aide de l'API DPAPI.
*   Transformation des appareils en proxies résidentiels.
*   Campagne orchestrée impliquant plusieurs applications potentiellement malveillantes.

**Vulnérabilités :**
*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. La vulnérabilité réside dans la **tromperie des utilisateurs** et l'**installation non consentie de logiciels malveillants**.

**Recommandations :**
*   Se méfier des offres de logiciels gratuits provenant de sources non officielles, particulièrement lorsqu'elles sont promues par des publicités.
*   Télécharger les logiciels uniquement depuis les sites web officiels des éditeurs réputés.
*   Faire preuve de vigilance face aux demandes d'autorisation inhabituelles des applications.
*   Utiliser des solutions de sécurité à jour (antivirus, anti-malware).
*   Vérifier la légitimité des certificats de signature de code lorsque c'est possible.
*   Consulter les indicateurs de compromission (IoCs) fournis par les chercheurs en cybersécurité pour renforcer les défenses.

---
[Source](https://www.bleepingcomputer.com/news/security/tamperedchef-infostealer-delivered-through-fraudulent-pdf-editor/){:target="_blank"}
