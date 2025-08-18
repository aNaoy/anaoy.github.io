---
title: 'HR giant Workday discloses data breach after Salesforce attack'
date: 2025-08-18
permalink: /posts/2025/08/18/hr-giant-workday-discloses-data-breach-after-salesforce-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Accès Non Autorisé aux Données d'Entreprise chez Workday**

Workday, un fournisseur majeur de solutions de gestion des ressources humaines, a subi une compromission de données résultant d'une attaque par ingénierie sociale ciblant une plateforme CRM tierce. Les attaquants ont réussi à accéder à des informations d'affaires courantes, telles que les noms, adresses électroniques et numéros de téléphone, potentiellement pour mener d'autres campagnes d'ingénierie sociale. Il n'y a eu aucune indication d'accès aux environnements clients (tenants) ni aux données qu'ils contiennent.

Cette violation s'inscrit dans une campagne plus large visant les instances Salesforce, attribuée au groupe d'extorsion ShinyHunters. D'autres entreprises de renom ont été touchées par cette même campagne. Les attaquants exploitent des techniques d'ingénierie sociale et de Vishing (hameçonnage vocal) pour inciter les employés des entreprises cibles à connecter une application malveillante à leurs instances Salesforce. Une fois cette connexion établie, les attaquants téléchargent et volent les bases de données des entreprises, utilisées ensuite pour l'extorsion.

**Points Clés:**

*   **Nature de la Compromission:** Accès non autorisé à des données d'entreprise via une plateforme CRM tierce.
*   **Impact sur Workday:** Exposition d'informations de contact professionnel (noms, e-mails, téléphones). Aucun accès aux données clients de Workday lui-même.
*   **Méthode d'Attaque:** Ingénierie sociale et Vishing ciblant les employés pour la connexion d'une application malveillante.
*   **Attribué à:** Le groupe d'extorsion ShinyHunters.
*   **Contexte:** Fait partie d'une vague d'attaques plus large ciblant les plateformes Salesforce d'autres organisations.

**Vulnérabilités:**

*   Bien qu'aucun CVE spécifique ne soit mentionné dans l'article pour la plateforme CRM tierce, la vulnérabilité réside dans la confiance accordée à une application OAuth malveillante après une ingénierie sociale réussie. La méthode d'attaque implique l'exploitation de la confiance des employés pour contourner les sécurités.

**Recommandations:**

*   **Sensibilisation et Formation:** Renforcer la formation des employés sur les risques d'ingénierie sociale, y compris les tentatives de Vishing et de hameçonnage.
*   **Vérification des Applications:** Mettre en place des politiques strictes pour la connexion d'applications tierces aux systèmes d'entreprise, particulièrement les plateformes cloud critiques comme Salesforce.
*   **Authentification Forte:** Encourager et imposer des méthodes d'authentification plus robustes pour limiter l'impact des informations d'identification compromises.
*   **Surveillance et Détection:** Maintenir une surveillance active des accès anormaux aux systèmes et des tentatives d'ingénierie sociale.

---
[Source](https://www.bleepingcomputer.com/news/security/hr-giant-workday-discloses-data-breach-amid-salesforce-attacks/){:target="_blank"}
