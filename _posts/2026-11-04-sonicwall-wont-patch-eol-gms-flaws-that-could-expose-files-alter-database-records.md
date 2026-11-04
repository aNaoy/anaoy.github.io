---
title: 'SonicWall Wont Patch EoL GMS Flaws That Could Expose Files, Alter Database Records'
date: 2026-11-04
permalink: /posts/2026/11/04/sonicwall-wont-patch-eol-gms-flaws-that-could-expose-files-alter-database-records/
tags:
- veille-cyber
- hackernews
---
### Absence de correctifs pour les failles critiques du système GMS de SonicWall

SonicWall a confirmé l'existence de deux vulnérabilités affectant les versions 9.5.2 et antérieures du Global Management System (GMS). Étant donné que ces produits sont en fin de vie (End-of-Life), l'éditeur a officiellement annoncé qu'aucun correctif ne serait déployé pour corriger ces failles.

**Points clés :**
* Les systèmes concernés sont obsolètes et ne bénéficieront plus de mises à jour de sécurité.
* Ces failles exposent les organisations à des risques élevés d'accès non autorisé à des données sensibles.
* Cette annonce fait suite à une période de vigilance accrue après l'exploitation active d'une autre vulnérabilité critique (CVE-2026-102255) identifiée récemment dans d'autres solutions de l'éditeur.

**Vulnérabilités identifiées :**
* **CVE-2026-109593 (Score CVSS 9.1) :** Vulnérabilité de lecture de fichiers non authentifiée, permettant à un attaquant distant d'accéder à des fichiers internes sensibles.
* **CVE-2026-109594 (Score CVSS 6.8) :** Vulnérabilité d'injection SQL nécessitant une authentification préalable, permettant de consulter ou de modifier les enregistrements de la base de données GMS.

**Recommandations :**
* **Migration impérative :** Les organisations utilisant encore SonicWall GMS 9.5.2 ou une version antérieure doivent migrer vers **SonicWall Network Security Manager (NSM)**.
* **Évaluation des risques :** Dans l'attente d'une migration, il est conseillé d'isoler ces systèmes des accès réseau non essentiels afin de limiter la surface d'exposition.

---
[Source](https://thehackernews.com/2026/11/sonicwall-wont-patch-eol-gms-flaws-that.html){:target="_blank"}
