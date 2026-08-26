---
title: 'Who Has Admin Rights in your Entra ID Directory&#x3f;, (Wed, Aug 26th)'
date: 2026-08-26
permalink: /posts/2026/08/26/who-has-admin-rights-in-your-entra-id-directoryx3f-wed-aug-26th/
tags:
- veille-cyber
- sans-isc
---
### Audit des privilèges d’administration dans Entra ID

La gestion des droits d'administration dans Entra ID est un enjeu critique de sécurité. L'accumulation de privilèges inutilisés ou excessifs, notamment par des anciens employés, des consultants ou des comptes oubliés, constitue un risque majeur de modification ou de suppression accidentelle/malveillante de ressources.

**Points clés :**
* **Conformité :** Le contrôle des privilèges d'administration est une exigence fondamentale des standards de sécurité (CIS Controls v7 #4 / v8 #6).
* **Principe du moindre privilège :** Il est impératif de limiter les droits d'accès en fonction des besoins réels (ex: un support technique ne devrait pas disposer de droits d'administrateur global).
* **Détection proactive :** Les listes d'administration doivent être régulièrement auditées pour identifier les comptes obsolètes ou les accès injustifiés.

**Vulnérabilités :**
* Cet article ne traite pas de CVE spécifiques, mais identifie des failles de configuration structurelles :
    * **Surprivilège :** Attribution de rôles (ex: Global Administrator) à des utilisateurs n'en ayant pas l'utilité fonctionnelle.
    * **Comptes résiduels :** Présence de comptes d'anciens collaborateurs, d'auditeurs tiers ou de prestataires dont les accès n'ont pas été révoqués.
    * **Shadow Admin :** Risque lié à l'attribution de rôles sensibles à des utilisateurs non techniques ou à des comptes de service oubliés.

**Recommandations :**
* **Audit automatisé :** Utiliser les scripts PowerShell fournis via Microsoft Graph (`Get-MgDirectoryRole` et `Get-MgDirectoryRoleMember`) pour extraire périodiquement la liste exhaustive des administrateurs.
* **Examen manuel :** Comparer la liste extraite avec l'organigramme réel et les responsabilités actuelles pour identifier les anomalies (ex: présence de "Global Reader" inattendus).
* **Nettoyage régulier :** Révoquer systématiquement les accès des comptes n'ayant plus de mission active et réduire les privilèges des comptes conservés au strict minimum nécessaire à leurs fonctions.

---
[Source](https://isc.sans.edu/diary/rss/33284){:target="_blank"}
