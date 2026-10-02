---
title: 'Dell asks admins to patch max severity CSM flaws as soon as possible'
date: 2026-10-02
permalink: /posts/2026/10/02/dell-asks-admins-to-patch-max-severity-csm-flaws-as-soon-as-possible/
tags:
- veille-cyber
- bleepingcomp
---
### Urgence sécuritaire : Correction critique pour les modules Dell CSM

Dell a publié un correctif pour plusieurs vulnérabilités de criticité maximale affectant ses modules de stockage conteneurisés (CSM) utilisés dans les environnements Kubernetes. Ces failles permettent à des attaquants non authentifiés de contourner les contrôles d'accès pour obtenir un contrôle administratif total sur l'infrastructure de stockage et les clusters.

**Points clés :**
* Les failles touchent principalement le module d'autorisation Dell CSM.
* La racine du problème réside dans une absence d'authentification pour des fonctions critiques.
* Bien qu'aucune exploitation active ne soit signalée pour ces vulnérabilités précises, les produits Dell sont régulièrement ciblés par des groupes étatiques (notamment Lazarus et UNC6201).

**Vulnérabilités identifiées :**
* **CVE-2026-63688 :** Accès aux identifiants administrateur du backend de stockage et contournement de l'autorisation.
* **CVE-2026-63692 :** Contournement de l'authentification dans le proxy d'autorisation et le service tenant.
* **CVE-2026-67269 :** Escalade de privilèges en tant que root sur les nœuds du cluster.
* **CVE-2026-54472 :** Accès administratif au proxy d'autorisation.
* **CVE-2026-61421 :** Falsification de jetons d'authentification pour obtenir des privilèges administrateur.
* **CVE-2026-67273 :** Contournement des contrôles d'accès Kubernetes pour une lecture non autorisée des secrets.

**Recommandations :**
* Mettre à jour immédiatement les modules Dell CSM vers la **version 1.18.0 ou ultérieure**.
* Appliquer ces correctifs en priorité absolue pour prévenir toute compromission de l'infrastructure de stockage et des données sensibles des locataires.

---
[Source](https://www.bleepingcomputer.com/news/security/new-max-severity-dell-csm-flaws-give-hackers-admin-privileges/){:target="_blank"}
