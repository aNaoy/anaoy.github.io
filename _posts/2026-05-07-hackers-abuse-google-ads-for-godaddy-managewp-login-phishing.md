---
title: 'Hackers abuse Google ads for GoDaddy ManageWP login phishing'
date: 2026-05-07
permalink: /posts/2026/05/07/hackers-abuse-google-ads-for-godaddy-managewp-login-phishing/
tags:
- veille-cyber
- bleepingcomp
---
### Phishing par publicité Google ciblant ManageWP

Une campagne de phishing sophistiquée détourne les résultats sponsorisés de Google pour usurper l'identité de ManageWP, une plateforme de gestion centralisée pour sites WordPress. Les attaquants utilisent une technique d'interception en temps réel (Adversary-in-the-Middle) pour voler les identifiants et les codes d'authentification à deux facteurs (2FA) des utilisateurs.

**Points clés :**
* **Vecteur d'attaque :** Publicités Google (Google Ads) positionnées au-dessus des résultats de recherche organiques pour la requête "managewp".
* **Mécanisme :** Le site frauduleux agit comme un proxy en temps réel, redirigeant les identifiants et les codes 2FA vers un canal Telegram contrôlé par les attaquants.
* **Impact :** Un seul compte ManageWP permet souvent de contrôler des centaines de sites web. Plus de 200 victimes ont déjà été identifiées.
* **Infrastructure :** Les attaquants utilisent un framework de phishing privé, potentiellement d'origine russophone, incluant des clauses de non-responsabilité juridique.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet incident, car il s'agit d'une attaque par ingénierie sociale (phishing) exploitant la confiance accordée aux résultats publicitaires de Google, et non d'une faille logicielle spécifique.

**Recommandations :**
* **Vérification des liens :** Inspectez systématiquement l'URL de destination avant de cliquer sur un résultat sponsorisé dans les moteurs de recherche.
* **Favoris :** Accédez aux services de gestion critiques via des signets (favoris) enregistrés localement plutôt que par une recherche Google à chaque connexion.
* **Gestion des accès :** Soyez vigilant face aux demandes de codes 2FA, surtout si le processus de connexion semble inhabituel ou lent (caractéristique des attaques AitM).
* **Sécurité des comptes :** En cas de doute, modifiez immédiatement votre mot de passe depuis le site officiel et révoquez les sessions actives si possible.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-abuse-google-ads-for-godaddy-managewp-login-phishing/){:target="_blank"}
