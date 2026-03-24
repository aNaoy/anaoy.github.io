---
title: 'HackerOne discloses employee data breach after Navia hack'
date: 2026-03-24
permalink: /posts/2026/03/24/hackerone-discloses-employee-data-breach-after-navia-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez HackerOne via le prestataire Navia

La plateforme de bug bounty HackerOne a été victime d'une fuite de données indirecte suite au piratage de son prestataire de services administratifs, Navia. Cet incident a compromis les informations personnelles de 287 employés.

**Points clés :**
*   **Incident :** Accès non autorisé aux systèmes de Navia entre le 22 décembre 2025 et le 15 janvier 2026.
*   **Données exposées :** Noms complets, numéros de sécurité sociale, adresses, numéros de téléphone, dates de naissance, emails et détails liés aux plans de couverture des employés et de leurs dépendants.
*   **Impact :** Bien qu'aucune information financière ou réclamation n'ait été touchée, les données exposées sont exploitables pour des campagnes de phishing et d'ingénierie sociale.

**Vulnérabilité :**
*   **Type :** BOLA (*Broken Object Level Authorization*). Bien qu'aucune CVE spécifique ne soit citée dans l'article, cette faille critique permet à un utilisateur non autorisé d'accéder à des objets (données) via une manipulation des identifiants dans les requêtes API.

**Recommandations :**
*   **Pour les employés concernés :** 
    *   Surveiller les comptes financiers pour toute activité suspecte.
    *   Renouveler les mots de passe et les questions de sécurité utilisant les données personnelles compromises.
    *   Activer les services de protection d'identité et de surveillance de crédit offerts par le prestataire.
*   **Conseil général :** Maintenir une vigilance accrue face aux messages entrants (phishing) exploitant les données personnelles dérobées.

---
[Source](https://www.bleepingcomputer.com/news/security/hackerone-discloses-employee-data-breach-after-navia-hack/){:target="_blank"}
