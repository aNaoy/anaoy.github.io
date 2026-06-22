---
title: 'A Glimpse into the “Search Your Target” Market for Stolen Credentials'
date: 2026-06-22
permalink: /posts/2026/06/22/a-glimpse-into-the-search-your-target-market-for-stolen-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### L'émergence des services de recherche à la demande pour identifiants volés

Le marché cybercriminel évolue avec l'apparition de services spécialisés de « recherche ciblée » de données. Plutôt que d'acheter des bases de données massives (dumps) difficiles à exploiter, les attaquants peuvent désormais payer des courtiers pour extraire, filtrer et formater des identifiants (e-mails, mots de passe, accès VPN, etc.) visant une entreprise, un domaine ou une zone géographique spécifique à partir de logs provenant de logiciels malveillants de type *infostealer*.

**Points clés** :
* **Modèle économique** : Ces acteurs agissent comme des processeurs de données, indexant des milliards de lignes d'identifiants pour offrir un service de recherche rapide et personnalisé.
* **Chaîne d'attaque** : Ce service se situe entre l'infection par *infostealer* et l'usurpation de compte (ATO), facilitant la préparation d'attaques ciblées.
* **Disparité qualitative** : Les retours d'utilisateurs sur les forums underground révèlent un écart entre les promesses publicitaires et la réalité : les bases contiennent souvent des doublons, des données obsolètes ou invalides.
* **Cadre tactique** : Ces activités correspondent aux tactiques MITRE ATT&CK **T1589.001** (Collecte d'informations d'identité) et **T1650** (Acquisition d'accès).

**Vulnérabilités** :
Il n'y a pas de CVE spécifique mentionnée, car il s'agit d'un problème lié à la **compromission des postes de travail par des infostealers** et au recyclage de données d'authentification volées. Les risques majeurs concernent la réutilisation des mots de passe et l'insuffisance des mécanismes d'authentification.

**Recommandations** :
* **Surveillance proactive** : Surveiller les forums du dark web pour détecter si les identifiants ou les domaines de l'organisation apparaissent dans ces bases de données de recherche.
* **Renforcement de l'authentification** : Généraliser l'usage de l'authentification multifacteur (MFA) pour neutraliser l'efficacité des identifiants volés.
* **Gestion des accès** : Réinitialiser rapidement les mots de passe et révoquer les sessions actives dès qu'une exposition est suspectée ou confirmée.
* **Hygiène numérique** : Sensibiliser les employés aux risques des logiciels malveillants qui dérobent les données de navigation et les identifiants enregistrés localement.

---
[Source](https://www.bleepingcomputer.com/news/security/a-glimpse-into-the-search-your-target-market-for-stolen-credentials/){:target="_blank"}
