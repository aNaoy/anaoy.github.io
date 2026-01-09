---
title: 'Russian APT28 Runs Credential-Stealing Campaign Targeting Energy and Policy Organizations'
date: 2026-01-09
permalink: /posts/2026/01/09/russian-apt28-runs-credential-stealing-campaign-targeting-energy-and-policy-organizations/
tags:
- veille-cyber
- hackernews
---
**Campagne de Phishing de APT28 Ciblant les Organisations Énergétiques et Politiques**

Des acteurs de menace parrainés par l'État russe, identifiés comme APT28 (également connu sous le nom de BlueDelta), ont mené une campagne sophistiquée de collecte d'identifiants. Cette campagne a ciblé des individus au sein d'une agence turque de recherche sur l'énergie et le nucléaire, ainsi que du personnel affilié à des groupes de réflexion européens, des organisations en Macédoine du Nord et en Ouzbékistan.

**Points Clés:**

*   **Ciblage Géographique et Sectoriel:** Les attaques ont été spécifiquement adaptées avec du contenu en turc et des leurres régionaux, démontrant un intérêt pour les organisations liées à la recherche énergétique, à la coopération en matière de défense et aux réseaux de communication gouvernementaux pertinents pour les objectifs de renseignement russes.
*   **Techniques de Phishing Avancées:** Les acteurs de la menace ont utilisé de fausses pages de connexion ressemblant à des services légitimes tels que Microsoft Outlook Web Access (OWA), Google et les portails VPN Sophos.
*   **Évasion des Détections:** Après avoir saisi leurs identifiants sur les fausses pages, les victimes étaient redirigées vers les sites légitimes, ce qui permettait d'éviter de déclencher des alertes.
*   **Utilisation d'Infrastructures Légitimes et Jetables:** La campagne a exploité des services tels que Webhook[. ]site, InfinityFree, Byet Internet Services et ngrok pour héberger les pages de phishing, exfiltrer les données volées et gérer les redirections. L'abus constant de ces infrastructures souligne la dépendance du groupe vis-à-vis de services jetables.
*   **Utilisation de Documents Leurre Crédibles:** Des documents PDF légitimes, notamment des rapports sur des conflits géopolitiques récents et des initiatives politiques, ont été utilisés comme leurres pour augmenter la crédibilité des emails de phishing.
*   **Chaîne d'Attaque Typique:** L'attaque commence par un email de phishing contenant un lien raccourci qui redirige la victime vers une page hébergée sur webhook[. ]site. Cette page affiche brièvement le document leurre avant de rediriger vers une fausse page de connexion qui capture les identifiants et les transmet à un point de terminaison webhook.

**Vulnérabilités / Tactiques:**

Bien que l'article ne mentionne pas de CVE spécifiques, les tactiques employées se basent sur des techniques de phishing et d'ingénierie sociale bien établies qui exploitent la confiance des utilisateurs dans les services familiers et les documents d'apparence légitime. Les vulnérabilités exploitées sont principalement liées au comportement humain et à la capacité des attaquants à créer des expériences en ligne trompeuses.

**Recommandations:**

*   **Vigilance Accrue Face aux Emails Suspects:** Les utilisateurs doivent faire preuve d'une extrême prudence face aux emails contenant des liens ou demandant des informations d'identification.
*   **Vérification des URL:** Il est crucial de vérifier attentivement l'URL avant de cliquer sur un lien ou de saisir des informations. Les redirections vers des domaines inconnus ou légèrement modifiés sont un signal d'alarme.
*   **Authentification Multi-Facteurs (MFA):** La mise en œuvre et l'utilisation de l'authentification multi-facteurs constituent une défense essentielle contre le vol d'identifiants.
*   **Formation à la Cybersécurité:** Des formations régulières sur la sensibilisation aux menaces, en particulier sur les techniques de phishing, sont indispensables pour le personnel des organisations ciblées.
*   **Surveillance et Blocage des Services Connus:** Les équipes de sécurité devraient envisager de surveiller et, si possible, de bloquer l'utilisation des services couramment exploités par ces groupes, tels que webhook[. ]site et les fournisseurs d'hébergement gratuits.

---
[Source](https://thehackernews.com/2026/01/russian-apt28-runs-credential-stealing.html){:target="_blank"}
