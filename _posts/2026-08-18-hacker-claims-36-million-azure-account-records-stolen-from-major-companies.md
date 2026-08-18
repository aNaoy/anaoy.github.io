---
title: 'Hacker claims 3.6 million Azure account records stolen from major companies'
date: 2026-08-18
permalink: /posts/2026/08/18/hacker-claims-36-million-azure-account-records-stolen-from-major-companies/
tags:
- veille-cyber
- bleepingcomp
---
### Vaste fuite de données Azure : 3,6 millions d'enregistrements compromis

Un acteur malveillant, connu sous le pseudonyme « TheHatman », revend sur le darknet des bases de données d'employés appartenant à plusieurs entreprises du classement Fortune 500 (notamment McDonald's, Vodafone, TCS et Gap Inc.). Au total, 3,64 millions de dossiers internes, extraits d'environnements Microsoft Azure/Entra, seraient exposés.

**Points clés :**
*   **Contenu des fuites :** Les données incluent des noms, identifiants employés, emails, postes, numéros de téléphone, adresses postales et informations sur les comptes de service (tenant).
*   **Vecteur d'attaque présumé :** L'attaquant affirme avoir utilisé des identifiants compromis via des techniques de « password spraying » (pulvérisation de mots de passe) et de fatigue MFA.
*   **Contradiction des entreprises :** Si certains experts en cybersécurité jugent les données authentiques et structurellement cohérentes avec des annuaires d'entreprise, plusieurs sociétés visées (dont TCS et Gap Inc.) ont nié toute intrusion récente, précisant que les données semblent obsolètes (vieilles de plusieurs années) et non critiques.

**Vulnérabilités :**
*   **Absence de CVE spécifique :** La faille repose sur l'exploitation d'identifiants valides et non sur une vulnérabilité logicielle logicielle propre à Azure.
*   **Risque majeur :** La présence de comptes de service et de noms d'administrateurs globaux dans les données facilite les campagnes de phishing ciblé et d'ingénierie sociale.

**Recommandations :**
*   **Renforcement du MFA :** Mettre en œuvre des méthodes d'authentification résistantes au phishing (ex: clés de sécurité FIDO2) pour contrer la « fatigue MFA ».
*   **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement pour les comptes de service, souvent ciblés pour leur accès prolongé aux infrastructures.
*   **Audit d'annuaire :** Réaliser régulièrement des nettoyages des comptes obsolètes dans l'Active Directory/Entra ID pour limiter l'impact en cas de fuite de données anciennes.
*   **Surveillance proactive :** Surveiller les fuites de credentials sur les forums spécialisés pour identifier toute exposition d'identifiants internes avant une éventuelle exploitation.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-claims-36-million-azure-account-records-stolen-from-major-companies/){:target="_blank"}
