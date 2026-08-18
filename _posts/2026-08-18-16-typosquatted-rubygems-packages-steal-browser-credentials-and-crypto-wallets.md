---
title: '16 Typosquatted RubyGems Packages Steal Browser Credentials and Crypto Wallets'
date: 2026-08-18
permalink: /posts/2026/08/18/16-typosquatted-rubygems-packages-steal-browser-credentials-and-crypto-wallets/
tags:
- veille-cyber
- hackernews
---
### Campagne de typosquatting sur RubyGems : Le malware "StubMaker"

Une campagne malveillante a été identifiée sur le dépôt **RubyGems**, utilisant 16 paquets au nom similaire à des dépendances populaires (**typosquatting**) pour déployer un infostealer sur Windows. Baptisée **StubMaker**, cette attaque exploite les mécanismes d'installation automatique pour compromettre des données sensibles.

#### Points clés
*   **Mécanisme d'infection :** Le script `extconf.rb`, exécuté automatiquement lors de l'installation, télécharge une charge utile Rust, qui exécute ensuite un malware en Go ("wincfg").
*   **Objectifs :** Vol de mots de passe de navigateurs (contournant la protection *App-Bound Encryption*), portefeuilles de cryptomonnaies, phrases secrètes (seed phrases), données Telegram et historique de navigation.
*   **Exploitation des failles de RubyGems :** Les attaquants tirent profit de la possibilité de réclamer des espaces de noms de paquets supprimés et de l'absence de validation des champs "Auteur", permettant de masquer l'origine réelle des paquets.
*   **Exfiltration :** Les données sont compressées dans des archives ZIP protégées, envoyées via Gofile, avec le lien de téléchargement transmis vers un serveur distant via HTTP non chiffré.

#### Vulnérabilités et vecteurs d'attaque
*   **CVE :** Aucune CVE spécifique n'est associée, l'attaque repose sur des **faiblesses de conception** (design flaws) de RubyGems plutôt que sur un bug logiciel classique.
*   **Vecteur principal :** Utilisation abusive des hooks de cycle de vie (`extconf.rb`) et du mécanisme de réutilisation de noms de paquets après suppression (*yanking*).

#### Recommandations
*   **Vigilance accrue :** Vérifier systématiquement l'orthographe exacte des dépendances avant toute installation (`bundle install`).
*   **Audit des dépendances :** Auditer les fichiers `Gemfile` pour identifier des paquets suspects ou peu connus récemment ajoutés.
*   **Isolation :** Utiliser des environnements isolés (conteneurs, machines virtuelles) pour tester de nouveaux paquets ou des dépendances tierces.
*   **Gestion des versions :** Fixer les versions des dépendances dans un fichier `Gemfile.lock` pour éviter les mises à jour automatiques vers des versions compromises (typosquattées).
*   **Sécurité des postes de travail :** Maintenir les solutions EDR/antivirus à jour, car ces outils peuvent détecter le comportement suspect des loaders (téléchargements externes, exécution de scripts non autorisés).

---
[Source](https://thehackernews.com/2026/08/16-typosquatted-rubygems-packages-steal.html){:target="_blank"}
