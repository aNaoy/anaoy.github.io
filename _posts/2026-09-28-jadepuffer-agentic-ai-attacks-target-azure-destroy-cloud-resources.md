---
title: 'JadePuffer agentic AI attacks target Azure, destroy cloud resources'
date: 2026-09-28
permalink: /posts/2026/09/28/jadepuffer-agentic-ai-attacks-target-azure-destroy-cloud-resources/
tags:
- veille-cyber
- bleepingcomp
---
### Menace JadePuffer : Attaques automatisées par IA sur Azure

Le groupe Storm-3168 (JadePuffer) exploite des agents d'intelligence artificielle pour automatiser des campagnes destructrices contre les environnements Azure. Ces attaques, qui ciblent les ressources cloud (machines virtuelles, bases de données, Key Vaults) et les infrastructures d'IA (datasets d'entraînement, bases vectorielles), visent à exfiltrer des identifiants et à supprimer des services critiques pour entraver les capacités de restauration.

**Points clés :**
*   **Automatisation par IA :** Utilisation d'agents pour la reconnaissance, le mouvement latéral et l'exécution de charges destructrices (ex: outil *EncForge*).
*   **Vecteur d'attaque :** Compromission de « Service Principals » (identités de service), dont certaines ont été exposées accidentellement sur des dépôts publics comme GitHub.
*   **Impact opérationnel :** Suppression rapide de ressources (plus de 100 comptes de stockage en 7 minutes) et neutralisation des mécanismes de sauvegarde et de récupération.
*   **Résilience observée :** Les verrous de ressources Azure (« Resource Locks ») et les protections au niveau des comptes de stockage ont permis de bloquer certaines suppressions, tout comme l'utilisation d'API non prises en charge pour les bases SQL Azure.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, l'attaque reposant sur l'abus d'identités légitimes (**Service Principals**) et sur une mauvaise gestion des secrets (exposition de clés dans des dépôts publics).

**Recommandations :**
*   **Principe du moindre privilège :** Auditer et restreindre strictement les permissions RBAC (Role-Based Access Control) des Service Principals.
*   **Protection des secrets :** Scanner activement les dépôts de code (publics et privés) pour détecter toute exposition accidentelle de jetons ou d'identifiants.
*   **Renforcement Azure :** Activer systématiquement les verrous de ressources (*Azure Resource Locks*) sur les composants critiques pour empêcher toute suppression accidentelle ou malveillante.
*   **Surveillance :** Activer les solutions de protection des charges de travail cloud (CWPP) pour détecter des comportements anormaux générés par des agents automatisés.

---
[Source](https://www.bleepingcomputer.com/news/security/jadepuffer-agentic-ai-attacks-target-azure-destroy-cloud-resources/){:target="_blank"}
