---
title: 'Police suspects Dutch hackers were involved in Odido breach'
date: 2026-07-10
permalink: /posts/2026/07/10/police-suspects-dutch-hackers-were-involved-in-odido-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Enquête sur la cyberattaque de l'opérateur Odido

La police néerlandaise a identifié des indices probants impliquant des pirates locaux dans le piratage du fournisseur de télécommunications Odido, survenu en février dernier. L'attaque a conduit au vol des données personnelles de 6,2 millions de clients.

**Points clés :**
*   **Mode opératoire :** Les attaquants ont utilisé l'ingénierie sociale (vishing). Un individu se faisant passer pour un employé informatique a contacté le service client d'Odido, induisant le personnel en erreur pour faciliter l'accès au système.
*   **Impact :** Le groupe de cybercriminels « ShinyHunters » a revendiqué l'attaque et publié 88 Go de données sur le dark web, incluant des noms, adresses, numéros de mobile, e-mails, IBAN et dates de naissance.
*   **Groupe de menace :** ShinyHunters est un collectif connu pour ses campagnes de phishing et de vishing ciblant les systèmes d'authentification unique (SSO) pour infiltrer les applications SaaS d'entreprises majeures.

**Vulnérabilités :**
*   **Facteur humain :** La vulnérabilité principale exploitée est la manipulation psychologique du support technique (vishing), permettant de contourner les protections logiques.
*   **Absence de CVE spécifique :** L'incident ne repose pas sur une faille logicielle répertoriée (CVE), mais sur une vulnérabilité procédurale. Cependant, le groupe est coutumier de l'exploitation de failles zero-day (ex: Oracle PeopleSoft) pour ses intrusions.

**Recommandations :**
*   **Renforcement du support client :** Mettre en place des protocoles de vérification d'identité stricts et obligatoires pour toute demande provenant d'un employé interne ou d'un service technique.
*   **Sensibilisation :** Former le personnel à reconnaître les tactiques de vishing et à ne jamais divulguer d'informations sensibles par téléphone, même face à une personne se présentant comme faisant partie de l'organisation.
*   **Sécurisation des accès :** Implémenter une authentification multifacteur (MFA) résistante au phishing (ex: clés FIDO2) pour l'accès aux systèmes critiques et aux comptes SSO.
*   **Détection et réponse :** Utiliser des solutions de simulation de brèche et d'attaque pour tester la réactivité des outils de surveillance (SIEM/EDR) face à des tactiques d'ingénierie sociale.

---
[Source](https://www.bleepingcomputer.com/news/security/police-suspects-dutch-hackers-were-involved-in-odido-breach/){:target="_blank"}
