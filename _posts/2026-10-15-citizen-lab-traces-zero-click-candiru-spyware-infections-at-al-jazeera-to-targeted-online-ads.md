---
title: 'Citizen Lab Traces Zero-Click Candiru Spyware Infections at Al Jazeera to Targeted Online Ads'
date: 2026-10-15
permalink: /posts/2026/10/15/citizen-lab-traces-zero-click-candiru-spyware-infections-at-al-jazeera-to-targeted-online-ads/
tags:
- veille-cyber
- hackernews
---
### Espionnage via publicités ciblées : La menace Candiru

Des chercheurs du Citizen Lab ont révélé une campagne d'espionnage sophistiquée utilisant des publicités en ligne pour infecter des appareils sans aucune interaction de l'utilisateur (attaque « zero-click »). Cette méthode a été utilisée pour cibler des employés de la chaîne Al Jazeera.

**Points clés :**
* **Vecteur d'attaque :** Des publicités injectées via la société « Discover-Tech ». Le code malveillant se déclenche automatiquement lors du chargement de la publicité, même si celle-ci est invisible à l'utilisateur.
* **Mécanisme :** La publicité transmet l'identifiant publicitaire et l'adresse IP de la victime à un serveur. Si l'appareil est jugé cible, le serveur déploie le logiciel espion Candiru.
* **Portée :** La campagne est massive. Entre mars et juin 2026, des milliards d'enchères publicitaires ont été effectuées, touchant potentiellement des dizaines de milliers de sites et d'applications, incluant des réseaux sensibles (OTAN, ONU, UE, gouvernements).
* **Attribution :** Le lien avec le spyware Candiru a été confirmé par l'analyse technique de fichiers Windows récupérés sur un appareil infecté, présentant des similitudes avec des outils identifiés en 2021.

**Vulnérabilités :**
* Bien qu'aucune CVE spécifique ne soit mentionnée pour l'exploit initial (qui permet de briser la sécurité du navigateur ou de l'application), la vulnérabilité réside dans la confiance accordée au système de diffusion publicitaire et l'exécution automatisée de code provenant de serveurs tiers non vérifiés.

**Recommandations :**
* **Analyse des logs :** Les organisations doivent surveiller leurs journaux de trafic pour détecter une séquence de connexion suspecte : une requête vers un serveur publicitaire (ex: `mtrtb.com`), suivie d'un appel vers un serveur de filtrage Candiru, puis vers un serveur de commande et de contrôle (C2).
* **Indicateurs de compromission :** Bloquer les domaines associés à Discover-Tech et rechercher le hash SHA-256 du logiciel espion : `255869de85e2a171993fc5eb8a556d873a1b8966e040f6f55926f2fa2d595cc8`.
* **Réponse immédiate :** Google et d'autres plateformes publicitaires ont déjà banni Discover-Tech. Il est conseillé de consulter les rapports complets de Citizen Lab et Confiant pour obtenir la liste exhaustive des serveurs C2 à bloquer.

---
[Source](https://thehackernews.com/2026/10/citizen-lab-traces-zero-click-candiru.html){:target="_blank"}
