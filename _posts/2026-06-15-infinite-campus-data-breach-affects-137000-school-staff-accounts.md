---
title: 'Infinite Campus data breach affects 137,000 school staff accounts'
date: 2026-06-15
permalink: /posts/2026/06/15/infinite-campus-data-breach-affects-137000-school-staff-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez Infinite Campus : 137 000 comptes compromis

Le groupe de cybercriminels ShinyHunters a revendiqué le vol de données personnelles concernant plus de 137 000 membres du personnel scolaire via une intrusion dans l'instance Salesforce de la société Infinite Campus, un fournisseur majeur de systèmes d'information pour le secteur éducatif (K-12).

**Points clés :**
*   **Victimes :** 137 100 comptes de personnel scolaire ont été impactés.
*   **Nature des données :** Les informations dérobées comprennent des noms, adresses e-mail, numéros de téléphone, adresses physiques, identifiants de connexion, postes occupés et des tickets de support client.
*   **Mode opératoire :** Les attaquants ont ciblé l'instance Salesforce de l'entreprise, une tactique récurrente de ShinyHunters qui multiplie les campagnes contre les utilisateurs de cette plateforme.
*   **Limitation :** Infinite Campus a précisé que les bases de données clients principales (données des élèves) ne semblent pas avoir été compromises.

**Vulnérabilités :**
Aucune CVE spécifique n'a été attribuée à cet incident, car l'attaque résulte d'une compromission de compte ou d'une mauvaise configuration de l'instance Salesforce plutôt que d'une vulnérabilité logicielle documentée. Le groupe ShinyHunters est toutefois connu pour exploiter activement diverses failles (notamment des vulnérabilités "zero-day" dans des suites logicielles d'entreprise comme Oracle PeopleSoft) pour mener ses campagnes d'extorsion.

**Recommandations :**
*   **Renforcement des accès :** Imposer l'authentification multifacteur (MFA) sur tous les accès aux instances SaaS (Salesforce, etc.).
*   **Gestion des accès tiers :** Auditer régulièrement les autorisations accordées aux applications tierces et aux intégrations Cloud.
*   **Surveillance proactive :** Utiliser des outils de simulation de brèche et d'attaque pour tester la réactivité des systèmes de détection (SIEM/EDR), car les alertes sur les intrusions réussies sont souvent sous-évaluées par les équipes de sécurité.
*   **Vigilance accrue :** Les personnes dont les données ont été exposées doivent rester vigilantes face aux tentatives de phishing et d'ingénierie sociale, leurs coordonnées étant désormais disponibles dans des archives diffusées sur le dark web.

---
[Source](https://www.bleepingcomputer.com/news/security/infinite-campus-data-breach-affects-137-000-school-staff-accounts/){:target="_blank"}
