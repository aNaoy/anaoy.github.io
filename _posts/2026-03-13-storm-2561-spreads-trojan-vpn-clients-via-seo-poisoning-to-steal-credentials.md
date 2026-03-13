---
title: 'Storm-2561 Spreads Trojan VPN Clients via SEO Poisoning to Steal Credentials'
date: 2026-03-13
permalink: /posts/2026/03/13/storm-2561-spreads-trojan-vpn-clients-via-seo-poisoning-to-steal-credentials/
tags:
- veille-cyber
- hackernews
---
### Campagne de vol d'identifiants VPN par Storm-2561 via SEO Poisoning

Le groupe cybercriminel **Storm-2561** mène une campagne sophistiquée visant à dérober des identifiants VPN d'entreprise. En manipulant les résultats des moteurs de recherche (SEO poisoning), les attaquants redirigent les utilisateurs vers des sites frauduleux proposant de faux logiciels VPN. Une fois installé, le malware (une variante de l'infostealer **Hyrax**) affiche une fausse fenêtre de connexion pour capturer les identifiants de la victime avant de la rediriger vers le site légitime pour lever tout soupçon.

**Points clés :**
* **Technique :** Utilisation du SEO poisoning pour apparaître dans les résultats de recherche de logiciels légitimes (ex: Pulse Secure, Ivanti).
* **Vecteur d'infection :** Téléchargement de fichiers ZIP hébergés sur GitHub contenant des installeurs MSI piégés.
* **Persistance :** Le malware utilise la clé de registre Windows *RunOnce* pour se lancer automatiquement à chaque redémarrage.
* **Crédibilité :** Les composants malveillants sont signés numériquement (certificat émis par *Taiyuan Lihua Near Information Technology Co., Ltd.*).
* **Vulnérabilités :** Pas de CVE spécifique mentionnée ; l'attaque repose sur l'ingénierie sociale et l'abus de la confiance accordée aux résultats des moteurs de recherche et aux signatures numériques.

**Recommandations :**
* **Vérification :** Télécharger uniquement les logiciels depuis les sites officiels des éditeurs et vérifier l'authenticité des sources.
* **Sécurité des comptes :** Généraliser l'utilisation de l'authentification multifacteur (MFA) sur tous les services, en particulier pour les accès VPN.
* **Sensibilisation :** Former les utilisateurs à la méfiance face aux résultats publicitaires ou aux sites tiers proposant des logiciels professionnels.

---
[Source](https://thehackernews.com/2026/03/storm-2561-spreads-trojan-vpn-clients.html){:target="_blank"}
