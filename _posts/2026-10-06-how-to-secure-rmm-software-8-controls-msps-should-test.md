---
title: 'How to secure RMM software: 8 controls MSPs should test'
date: 2026-10-06
permalink: /posts/2026/10/06/how-to-secure-rmm-software-8-controls-msps-should-test/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des outils RMM : 8 contrôles essentiels pour les MSP

Les logiciels de surveillance et de gestion à distance (RMM) constituent une cible privilégiée pour les attaquants, car ils offrent un accès administratif étendu à de nombreux environnements clients. La compromission d'un seul compte privilégié peut entraîner une propagation massive des menaces.

#### Vulnérabilités et incidents notables
Les récentes attaques soulignent la criticité du plan de gestion :
*   **CVE-2026-86218 :** faille RCE (exécution de code à distance) pré-authentification critique dans la plateforme N-central de N-able.
*   **CVE-2025-53770 et CVE-2025-53771 :** vulnérabilités "ToolShell" dans Microsoft SharePoint exploitées avant la publication de correctifs.

#### Points clés pour l'évaluation des outils
Au-delà du nombre de fonctionnalités, les MSP doivent privilégier la continuité des flux de travail (de la détection à la restauration) et tester des scénarios réels (échecs de correctifs, comptes compromis, scripts non autorisés).

#### Recommandations : Les 8 contrôles à tester
1.  **Découverte et inventaire :** Identification continue et classification automatique de tous les terminaux et actifs logiciels.
2.  **Gestion des correctifs basée sur les risques :** Priorisation des mises à jour, gestion des échecs de déploiement et capacités de retour arrière (rollback).
3.  **Contrôle d'accès et privilèges :** Implémentation stricte de l'authentification multifacteur (MFA), du contrôle d'accès basé sur les rôles (RBAC) et de la séparation des tâches.
4.  **Priorisation des alertes :** Réduction de la fatigue liée aux alertes grâce à une visibilité contextuelle permettant de distinguer les incidents critiques des tâches routinières.
5.  **Automatisation sécurisée :** Mise en place de contrôles d'approbation et d'audits rigoureux pour toute exécution de scripts privilégiés.
6.  **Intégration opérationnelle :** Interopérabilité fluide entre les outils de sécurité (EDR/XDR) et la gestion, permettant de passer rapidement de l'investigation à la remédiation.
7.  **Préparation à la restauration :** Intégration de la sauvegarde et du scan anti-malware des points de restauration pour garantir l'intégrité des systèmes rétablis.
8.  **Séparation des locataires et auditabilité :** Isolation stricte des données et des permissions entre les clients, couplée à des journaux d'audit détaillés pour la conformité.

---
[Source](https://www.bleepingcomputer.com/news/security/how-to-secure-rmm-software-8-controls-msps-should-test/){:target="_blank"}
