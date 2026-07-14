---
title: 'SAP warns of critical flaws in NetWeaver and Commerce Cloud'
date: 2026-07-14
permalink: /posts/2026/07/14/sap-warns-of-critical-flaws-in-netweaver-and-commerce-cloud/
tags:
- veille-cyber
- bleepingcomp
---
### Correctifs de sécurité critiques pour les solutions SAP

SAP a publié ses mises à jour de juillet 2026, corrigeant un total de 16 vulnérabilités affectant ses principales solutions d'entreprise. Trois failles critiques ont été identifiées dans NetWeaver, Commerce Cloud et AppRouter, exposant les infrastructures à des risques de corruption de mémoire, de manipulation de requêtes et d'accès non autorisés.

**Points clés :**
*   Le déploiement de ces correctifs est essentiel pour maintenir l'intégrité, la confidentialité et la disponibilité des systèmes SAP.
*   Aucune preuve d'exploitation active n'a été signalée pour ces failles spécifiques, bien que SAP soit une cible récurrente pour les cyberattaquants.
*   Outre les failles critiques, le correctif traite six vulnérabilités de sévérité élevée, sept de niveau moyen et une de niveau faible.

**Vulnérabilités critiques identifiées :**
*   **CVE-2026-44747 (NetWeaver AS ABAP) :** Problème de corruption de mémoire dû à une écriture hors limites. Permet à un attaquant authentifié d'accéder à des données, de les modifier ou de provoquer une indisponibilité du système.
*   **CVE-2026-27690 (SAP AppRouter) :** Vulnérabilité de type "HTTP Request Smuggling" exploitable par un attaquant non authentifié pour intercepter des réponses utilisateurs ou mener des attaques par déni de service (DoS).
*   **CVE-2026-44761 (SAP Commerce Cloud) :** Utilisation de identifiants par défaut permettant à un attaquant d'obtenir des jetons d'accès valides et de manipuler des données via les APIs.

**Recommandations :**
*   Appliquer sans délai les correctifs de sécurité fournis par SAP dans le cadre du cycle de mise à jour de juillet 2026.
*   Réviser les configurations de sécurité et les accès aux APIs pour Commerce Cloud afin de supprimer tout identifiant par défaut.
*   Surveiller les journaux d'accès pour détecter toute activité inhabituelle liée aux composants AppRouter et NetWeaver.

---
[Source](https://www.bleepingcomputer.com/news/security/sap-warns-of-critical-flaws-in-netweaver-and-commerce-cloud/){:target="_blank"}
