---
title: 'Microsoft plans to deprecate Windows Deployment Services'
date: 2026-09-25
permalink: /posts/2026/09/25/microsoft-plans-to-deprecate-windows-deployment-services/
tags:
- veille-cyber
- bleepingcomp
---
### Fin de support pour Windows Deployment Services (WDS)

Microsoft a annoncé l'abandon progressif du rôle de serveur Windows Deployment Services (WDS), utilisé pour le déploiement à distance d'OS sur des parcs informatiques. Cette suppression complète est prévue dans la prochaine version de Windows Server, marquant l'arrêt définitif de son développement, de ses outils de gestion et de sa fonctionnalité PXE (Preboot Execution Environment).

**Points clés :**
* **Évolution de la politique :** WDS a déjà subi plusieurs restrictions, notamment la suppression du support `boot.wim` en 2021 et la désactivation par défaut du déploiement "mains libres" en janvier 2026.
* **Périmètre :** La suppression concerne l'ensemble des services, interfaces et fonctionnalités PXE natifs de WDS.
* **Impact limité :** Les versions actuelles de Windows Server (2025 et antérieures) restent supportées selon leur cycle de vie habituel. Les solutions tierces et les implémentations PXE indépendantes ne sont pas affectées.
* **Microsoft Configuration Manager :** L'outil reste disponible, mais Microsoft recommande vivement de migrer les environnements utilisant encore le PXE ou le multicast basé sur WDS.

**Vulnérabilités :**
* **CVE-2026-0386 :** Cette vulnérabilité a conduit à la désactivation par défaut du déploiement "mains libres" dans les mises à jour Windows d'avril 2026 afin de renforcer la sécurité des déploiements.

**Recommandations :**
* **Planification de migration :** Les administrateurs IT doivent anticiper le retrait de WDS et migrer vers des solutions modernes de gestion du déploiement, telles que *Microsoft Configuration Manager*.
* **Audit des dépendances :** Identifier et décommissionner les dépendances aux fonctions PXE ou multicast héritées de WDS au sein des infrastructures actuelles.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-deprecate-windows-deployment-services-after-windows-server-2025/){:target="_blank"}
