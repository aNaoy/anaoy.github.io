---
title: 'New Windows LegacyHive zero-day gives hackers admin privileges'
date: 2026-07-17
permalink: /posts/2026/07/17/new-windows-legacyhive-zero-day-gives-hackers-admin-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité Zero-Day "LegacyHive" : Élévation de privilèges sous Windows

Le chercheur en sécurité "Nightmare Eclipse" a publié une preuve de concept (PoC) pour une vulnérabilité zero-day appelée **LegacyHive**, affectant le service de profil utilisateur de Windows. Cette faille permet à un utilisateur non privilégié d'élever ses droits en manipulant la base de registre.

**Points clés :**
*   **Mécanisme :** L'exploitation permet de monter la ruche de registre (`usrclass.dat`) d'un autre utilisateur, offrant la possibilité de modifier des entrées pour obtenir une exécution de code arbitraire lors de la connexion d'un administrateur.
*   **État du PoC :** La version publique actuelle a été volontairement limitée par son auteur, nécessitant des identifiants utilisateur supplémentaires, mais la vulnérabilité fondamentale reste exploitable de manière plus large.
*   **Réponse de Microsoft :** L'éditeur est conscient de la vulnérabilité et mène actuellement une enquête, tout en rappelant son engagement pour une divulgation coordonnée.
*   **Historique :** Le chercheur est à l'origine de nombreuses découvertes récentes sur Windows (RoguePlanet, BlueHammer, etc.), ce qui a généré des tensions avec Microsoft, allant jusqu'à des menaces d'action en justice de la part de l'entreprise.

**Vulnérabilités :**
*   **CVE :** Aucune assignée à ce jour.
*   **Composant impacté :** Windows User Profile Service.

**Recommandations :**
*   **Détection :** Utiliser les requêtes KQL (Kusto Query Language) publiées par des experts comme Kevin Beaumont pour identifier les tentatives d'exploitation via Microsoft Defender for Endpoint (MDE).
*   **Veille :** Surveiller les prochains bulletins de sécurité mensuels ("Patch Tuesday") de Microsoft pour l'application d'un correctif officiel dès sa publication.
*   **Limitation des accès :** Restreindre les privilèges des utilisateurs standards sur les systèmes sensibles pour limiter l'impact potentiel d'une escalade de privilèges.

---
[Source](https://www.bleepingcomputer.com/news/security/new-windows-legacyhive-zero-day-exploit-grants-hackers-admin-access/){:target="_blank"}
