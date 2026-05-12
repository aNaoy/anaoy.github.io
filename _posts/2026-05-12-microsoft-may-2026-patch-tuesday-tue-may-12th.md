---
title: 'Microsoft May 2026 Patch Tuesday, (Tue, May 12th)'
date: 2026-05-12
permalink: /posts/2026/05/12/microsoft-may-2026-patch-tuesday-tue-may-12th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du Patch Tuesday de Microsoft : Mai 2026

Le bulletin de sécurité de mai 2026 traite 137 vulnérabilités affectant les produits Microsoft, en plus de 137 correctifs dédiés à l'écosystème Chromium pour Microsoft Edge. Aucune de ces failles n'est actuellement listée comme étant divulguée publiquement ou exploitée activement.

**Points clés :**
*   **Portée :** 137 vulnérabilités corrigées dans l'écosystème Microsoft.
*   **Azure :** Plusieurs services critiques (Azure DevOps, Logic Apps, Managed Instance for Apache Cassandra) présentent des failles de sévérité "Critique". Pour les services Azure identifiés comme "no customer action required", aucune intervention directe des clients n'est nécessaire.
*   **Cibles privilégiées :** Les outils de développement et de CI/CD, tels que Jira et Confluence, sont particulièrement visés par les attaquants via des attaques sur la chaîne d'approvisionnement (*supply chain*).

**Vulnérabilités critiques à surveiller :**
*   **CVE-2026-41103 :** Élévation de privilèges dans le plugin Microsoft SSO pour Jira et Confluence.
*   **CVE-2026-41089 :** Exécution de code à distance (RCE) pré-authentification dans le service Netlogon.
*   **CVE-2026-42826 :** Divulgation d'informations dans Azure DevOps (Score CVSS 10.0).
*   **CVE-2026-33109 :** RCE dans Azure Managed Instance for Apache Cassandra.
*   **CVE-2026-41096 :** RCE dans le client DNS Windows.
*   **CVE-2026-40402 :** Élévation de privilèges dans Windows Hyper-V.

**Recommandations :**
1.  **Priorisation :** Appliquer en priorité les correctifs sur les serveurs exposés, en particulier ceux gérant le service Netlogon et les outils de développement (Jira/Confluence/Azure DevOps).
2.  **Gestion des services Cloud :** Bien que Microsoft gère les correctifs pour les services Azure marqués "no customer action required", il est conseillé de surveiller les bulletins de sécurité officiels pour les autres composants Azure qui, eux, nécessitent une mise à jour manuelle des agents.
3.  **Mise à jour client :** Déployer les mises à jour pour les produits Office (Word, Excel) et les composants Windows critiques (Client DNS, Hyper-V) pour limiter les vecteurs d'attaque par exécution de code.

---
[Source](https://isc.sans.edu/diary/rss/32980){:target="_blank"}
