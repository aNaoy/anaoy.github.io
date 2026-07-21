---
title: 'Estée Lauder discloses data breach via Oracle E-Business flaw'
date: 2026-07-21
permalink: /posts/2026/07/21/estee-lauder-discloses-data-breach-via-oracle-e-business-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez Estée Lauder via une faille Oracle

Estée Lauder a subi une violation de données affectant son système de gestion des ressources humaines, Oracle E-Business Suite. L'intrusion, survenue le 9 août 2025, a permis à des attaquants d'exfiltrer des informations personnelles sensibles.

**Points clés :**
* **Nature de l'incident :** Accès non autorisé à la suite Oracle E-Business utilisée pour la gestion RH.
* **Données exposées :** Noms complets, adresses postales et électroniques, dates de naissance, numéros de sécurité sociale, numéros de passeport, données bancaires, informations de santé et rapports d'emploi (paie et performance).
* **Contexte :** Cette attaque s'inscrit dans une campagne massive attribuée au groupe de ransomware Clop, ciblant de nombreuses organisations internationales.

**Vulnérabilité identifiée :**
* **CVE-2025-61882 :** Faille critique (zero-day au moment des faits) touchant les versions 12.2.3 à 12.2.14 d'Oracle E-Business Suite. Elle permettait de contourner l'authentification et d'exécuter du code à distance via le composant « BI Publisher Integration ».

**Recommandations :**
* **Pour les utilisateurs impactés :** Rester vigilant face aux risques d'usurpation d'identité et de fraude. Estée Lauder propose 24 mois de services de surveillance d'identité via Kroll.
* **Pour les entreprises :**
    * Appliquer immédiatement les correctifs de sécurité fournis par Oracle (disponibles depuis octobre 2025).
    * Maintenir une veille active sur les vulnérabilités affectant les outils métier critiques (ERP, systèmes RH).
    * Réaliser régulièrement des tests de simulation d'attaques pour valider l'efficacité des solutions de détection (SIEM/EDR).

---
[Source](https://www.bleepingcomputer.com/news/security/est-e-lauder-discloses-data-breach-via-oracle-e-business-flaw/){:target="_blank"}
