---
title: 'Nikkei discloses third data breach in a month, 1.8M records exposed'
date: 2026-10-20
permalink: /posts/2026/10/20/nikkei-discloses-third-data-breach-in-a-month-18m-records-exposed/
tags:
- veille-cyber
- bleepingcomp
---
### Troisième cyberattaque en un mois chez Nikkei : 1,8 million de dossiers exposés

Le géant japonais de l'information financière, Nikkei Inc., a subi une nouvelle violation de données le 7 octobre, la troisième en un mois. Des pirates informatiques ont utilisé des identifiants volés pour accéder à un système de développement hébergé dans le cloud.

**Points clés :**
* **Volume :** 1,83 million de dossiers exposés.
* **Nature des données :** 150 000 dossiers contiennent des informations sensibles (noms complets, emails, adresses, numéros de téléphone et dates de naissance). 1,68 million de dossiers ne contiennent aucune donnée identifiable.
* **Impact financier :** Aucune donnée de carte de crédit n'a été compromise. Aucun service n'a été interrompu.
* **Récurrence :** Cet incident fait suite à deux autres compromissions récentes impliquant des comptes Google Workspace et Microsoft 365 d'employés.

**Vulnérabilités :**
* Utilisation d'identifiants compromis pour contourner les accès légitimes.
* Accès non autorisé à un environnement de développement Cloud.
* *Note : Aucune référence CVE spécifique n'a été communiquée, l'incident reposant sur l'exploitation d'identifiants valides.*

**Recommandations :**
* **Renforcement de l'authentification :** Implémenter ou généraliser l'authentification multi-facteurs (MFA) robuste pour tous les comptes, particulièrement ceux accédant à des ressources cloud.
* **Gestion des accès (IAM) :** Révoquer systématiquement les accès obsolètes et mettre en œuvre le principe du moindre privilège.
* **Surveillance proactive :** Renforcer la détection des comportements anormaux sur les systèmes de développement, souvent moins sécurisés que les environnements de production.
* **Réponse aux incidents :** Maintenir une politique de notification transparente et rapide, conformément aux exigences réglementaires en vigueur (notamment auprès de la Personal Information Protection Commission).

---
[Source](https://www.bleepingcomputer.com/news/security/nikkei-discloses-third-data-breach-in-a-month-18m-records-exposed/){:target="_blank"}
