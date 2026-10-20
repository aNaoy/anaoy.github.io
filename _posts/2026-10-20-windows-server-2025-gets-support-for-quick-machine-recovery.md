---
title: 'Windows Server 2025 gets support for quick machine recovery'
date: 2026-10-20
permalink: /posts/2026/10/20/windows-server-2025-gets-support-for-quick-machine-recovery/
tags:
- veille-cyber
- bleepingcomp
---
### Déploiement du Quick Machine Recovery sur Windows Server 2025

Microsoft a étendu la fonctionnalité **Quick Machine Recovery (QMR)** à Windows Server 2025 suite à la mise à jour de sécurité d'octobre 2026. Cet outil permet de rétablir des systèmes incapables de démarrer (suite à une mise à jour défectueuse ou un problème de configuration) sans nécessiter d'accès physique au serveur.

**Points clés :**
* **Fonctionnement :** En cas d'échec de démarrage, le système bascule dans l'environnement de récupération Windows (WinRE) et exécute le QMR pour identifier et appliquer des correctifs via Windows Update.
* **Origine :** Développée dans le cadre de la « Windows Resiliency Initiative » après la panne mondiale majeure causée par la mise à jour CrowdStrike de juillet 2024.
* **État par défaut :** La remédiation via le cloud est désactivée par défaut sur Windows Server 2025.

**Vulnérabilités :**
* L'article ne mentionne aucune CVE spécifique. Le risque principal lié à cette fonctionnalité est lié à la dépendance envers des services cloud pour automatiser des modifications système sur des serveurs critiques.

**Recommandations :**
* **Activation :** Les administrateurs peuvent activer la remédiation cloud et automatique via la Stratégie de groupe (GPO) : *Configuration ordinateur > Modèles d'administration > Système > Quick Machine Recovery*.
* **Gestion centralisée :** L'activation nécessite des permissions d'édition sur les GPO et une liaison appropriée aux unités d'organisation (OU) cibles.
* **Désactivation :** Pour sécuriser les environnements ne souhaitant pas autoriser de correctifs externes automatiques, il est recommandé de désactiver explicitement les paramètres *Enable Cloud Remediation* et *Enable Auto Remediation* via l'éditeur de stratégie de groupe local ou de domaine.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-server-2025-gets-support-for-quick-machine-recovery/){:target="_blank"}
