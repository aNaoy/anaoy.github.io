---
title: 'Data breach at edtech giant McGraw Hill affects 13.5 million accounts'
date: 2026-04-16
permalink: /posts/2026/04/16/data-breach-at-edtech-giant-mcgraw-hill-affects-135-million-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive chez McGraw Hill via Salesforce

Le géant de l'édition éducative McGraw Hill a confirmé une violation de données touchant 13,5 millions de comptes utilisateurs. L'incident a été perpétré par le groupe de cybercriminels « ShinyHunters », qui a publié plus de 100 Go de données sur le dark web suite à une tentative d'extorsion.

**Points clés :**
* **Volume :** 13,5 millions de comptes compromis.
* **Nature des données exposées :** Noms, adresses physiques, numéros de téléphone et adresses e-mail.
* **Méthode :** Les attaquants ont exploité une mauvaise configuration au sein de l'environnement Salesforce utilisé par McGraw Hill.
* **Contexte :** McGraw Hill précise que l'incident est lié à une vulnérabilité plus large touchant plusieurs organisations utilisant les services de Salesforce.

**Vulnérabilités :**
* L'incident ne repose pas sur une faille logicielle spécifique (CVE), mais sur une **mauvaise configuration (misconfiguration) de l'environnement Salesforce**, permettant un accès non autorisé à des données hébergées sur une page web de la plateforme.

**Recommandations :**
* **Audit des configurations :** Les organisations utilisant des plateformes SaaS (comme Salesforce) doivent impérativement auditer régulièrement leurs paramètres de sécurité pour éviter toute exposition involontaire de données.
* **Vigilance accrue :** Étant donné la nature des données divulguées (noms, e-mails, téléphones), les utilisateurs concernés doivent être particulièrement vigilants face aux campagnes de **hameçonnage ciblé (spear-phishing)**.
* **Gestion des accès :** Appliquer le principe du moindre privilège sur les plateformes tierces pour limiter l'impact en cas de compromission d'une instance.

---
[Source](https://www.bleepingcomputer.com/news/security/data-breach-at-edtech-giant-mcgraw-hill-affects-135-million-accounts/){:target="_blank"}
