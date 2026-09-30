---
title: 'Bitget hacked via zero-day in third-party security products'
date: 2026-09-30
permalink: /posts/2026/09/30/bitget-hacked-via-zero-day-in-third-party-security-products/
tags:
- veille-cyber
- bleepingcomp
---
### Vol de 387,5 millions de dollars sur Bitget via une vulnérabilité tierce

La plateforme d'échange de cryptomonnaies Bitget a subi un piratage massif totalisant 387,5 millions de dollars. L'attaque a été orchestrée par des acteurs malveillants, suspectés d'être liés à la Corée du Nord, en exploitant des vulnérabilités de type "zero-day" au sein d'outils de sécurité tiers utilisés par la plateforme.

**Points clés :**
* **Chronologie :** Les premières intrusions ont débuté le 31 août 2026, avec des vols effectifs réalisés le 25 septembre sur une période de trois heures.
* **Méthodologie :** Les attaquants ont compromis deux appliances de sécurité tierces. Ils y ont installé des web shells et établi des connexions de commande et contrôle (C2) pour effectuer des mouvements latéraux vers le serveur de gestion des portefeuilles de production.
* **Impact :** Utilisation d'un outil de retrait personnalisé pour manipuler les données de transaction, forçant l'autorisation automatique de transferts illégitimes depuis les portefeuilles "chauds" et "tièdes".

**Vulnérabilités :**
* Aucune CVE n'a été spécifiquement attribuée à ce stade, l'incident reposant sur des **vulnérabilités zero-day** identifiées dans des produits de sécurité tiers non nommés.

**Recommandations :**
* **Audit des tiers :** Renforcer la surveillance et le cloisonnement des appliances de sécurité tierces intégrées au réseau de production.
* **Gestion des accès :** Appliquer le principe du moindre privilège pour limiter la propagation latérale en cas de compromission d'un nœud.
* **Surveillance proactive :** Détecter les anomalies dans les processus de service, notamment les accès non autorisés aux variables d'environnement contenant des identifiants sensibles.
* **Sécurité des flux :** Mettre en place des mécanismes de validation multi-niveaux pour les transactions automatisées afin d'éviter le contournement des processus d'autorisation par usurpation de données.

---
[Source](https://www.bleepingcomputer.com/news/security/bitget-hacked-via-zero-day-in-third-party-security-products/){:target="_blank"}
