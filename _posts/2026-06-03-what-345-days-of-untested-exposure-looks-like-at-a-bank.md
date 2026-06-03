---
title: 'What 345 Days of Untested Exposure Looks Like at a Bank'
date: 2026-06-03
permalink: /posts/2026/06/03/what-345-days-of-untested-exposure-looks-like-at-a-bank/
tags:
- veille-cyber
- bleepingcomp
---
### Le danger de l'exposition prolongée : Pourquoi les tests annuels sont insuffisants

Les institutions financières sont de plus en plus vulnérables en raison d'un décalage structurel : elles se reposent sur des tests d'intrusion annuels alors que leur surface d'attaque évolue quotidiennement (intégrations API, migrations cloud, portails tiers). Cet écart de 345 jours entre deux tests laisse aux attaquants une fenêtre d'opportunité considérable pour exploiter des failles non détectées.

**Points clés :**
*   **Obsolescence des tests annuels :** La conformité réglementaire (PCI DSS, FFIEC, NYDFS) impose des tests après chaque changement significatif, mais les entreprises continuent de traiter ces évaluations comme un événement discret annuel.
*   **Risque lié aux tiers :** Les portails gérés par des prestataires, mais hébergés sur des sous-domaines bancaires, constituent une « zone grise » souvent exclue des tests d'intrusion par erreur, alors qu'ils représentent une porte d'entrée majeure.
*   **Limites de l'automatisation :** Les scanners de vulnérabilités classiques ne détectent pas les failles logiques complexes (comme l'énumération d'identifiants ou le chaînage d'attaques), qui nécessitent une intervention humaine.

**Vulnérabilités identifiées :**
*   **IDOR (Insecure Direct Object Reference) :** Une faille sur un portail financier permettait, via la manipulation d'identifiants de locataires (tenant IDs) sur un endpoint API sans authentification, d'extraire des données nominatives (employés, emails, téléphones) appartenant à plusieurs institutions.
*   **Défaut de contrôle d'accès :** L'absence d'authentification et une politique CORS (Cross-Origin Resource Sharing) permissive permettaient à des sites tiers d'extraire des données ou d'injecter des demandes frauduleuses via le navigateur des utilisateurs.

**Recommandations :**
*   **Adopter le test continu :** Remplacer le modèle annuel par un programme de test qui réagit aux changements réels de l'infrastructure plutôt qu'à une date calendaire.
*   **Élargir la gestion de la surface d'attaque :** Inclure systématiquement les domaines et sous-domaines gérés par des tiers dans le périmètre de test si l'institution en est propriétaire ou les utilise.
*   **Prioriser l'expertise humaine :** Compléter l'automatisation par des tests humains capables d'identifier des scénarios d'exploitation complexes et d'évaluer l'impact réel des vulnérabilités sur les processus métier.

---
[Source](https://www.bleepingcomputer.com/news/security/what-345-days-of-untested-exposure-looks-like-at-a-bank/){:target="_blank"}
