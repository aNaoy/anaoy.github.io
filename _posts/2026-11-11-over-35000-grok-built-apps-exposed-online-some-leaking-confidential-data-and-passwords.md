---
title: 'Over 35,000 Grok-Built Apps Exposed Online, Some Leaking Confidential Data and Passwords'
date: 2026-11-11
permalink: /posts/2026/11/11/over-35000-grok-built-apps-exposed-online-some-leaking-confidential-data-and-passwords/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité majeure : Exposition massive de données via les applications Grok

Des chercheurs de la société Claroc ont identifié plus de 35 500 applications créées via l'outil "Grok Build" accessibles publiquement sans authentification. Ces applications, hébergées sur des sous-domaines `grok.me`, exposent des données sensibles allant de documents confidentiels d'entreprise (stratégies commerciales, annuaires d'employés) à des mots de passe en clair.

**Points clés :**
* **Risque par défaut :** L'option "Anyone with the link" (toute personne disposant du lien) est souvent sélectionnée par défaut, rendant les applications indexables via les services de DNS passifs.
* **Faille logique :** Même lorsque l'authentification est activée, le code généré par Grok présente des failles (ex: validation défaillante des accès via Google ou X), permettant à des utilisateurs non autorisés d'accéder aux données, de les modifier ou de les supprimer.
* **Étendue :** Le problème touche aussi bien des particuliers que des grandes entreprises (Fortune 500) et des entités gouvernementales.
* **Absence de CVE :** Aucune CVE n'est associée, car il s'agit d'une mauvaise configuration par défaut et de faiblesses dans le code généré par l'IA et non d'une faille logicielle isolée.

**Recommandations de sécurité :**
* **Audit des usages :** Recenser les outils de création d'applications par IA utilisés par les employés (Grok, Replit, v0, etc.).
* **Sécurisation des accès :** Configurer impérativement les applications contenant des données internes sur "Only you" ou "Invited users".
* **Tests d'intrusion manuels :** Vérifier systématiquement si une connexion avec un compte externe non autorisé permet l'accès aux données.
* **Veille DNS :** Utiliser des données de DNS passifs pour identifier si des sous-domaines de l'organisation ont été publiés.
* **Nettoyage :** Supprimer ("unpublish") les applications obsolètes et inspecter le code source à la recherche d'identifiants ou de données sensibles en clair.

---
[Source](https://thehackernews.com/2026/11/over-35000-grok-built-apps-exposed.html){:target="_blank"}
