---
title: 'Microsoft Patches CVSS 10.0 Azure AI Foundry Flaw Enabling Unauthorized Privilege Escalation'
date: 2026-09-18
permalink: /posts/2026/09/18/microsoft-patches-cvss-100-azure-ai-foundry-flaw-enabling-unauthorized-privilege-escalation/
tags:
- veille-cyber
- hackernews
---
### Correctifs critiques chez Microsoft : Azure AI Foundry et services cloud

Microsoft a récemment corrigé plusieurs vulnérabilités critiques permettant l'élévation de privilèges au sein de son écosystème cloud et de ses systèmes Windows.

**Points clés :**
*   Les failles affectant les services cloud (Azure) ont été corrigées directement par Microsoft ; aucune intervention utilisateur n'est requise.
*   Certaines vulnérabilités locales sur Windows 11 nécessitent l'installation de mises à jour cumulatives.
*   Aucune preuve d'exploitation active n'a été constatée pour les failles Azure, contrairement aux vulnérabilités ALPC récemment découvertes.

**Vulnérabilités majeures :**
*   **CVE-2026-85889 (CVSS 10.0) :** Absence d'authentification dans **Azure AI Foundry**, permettant une élévation de privilèges réseau.
*   **CVE-2026-85885 (CVSS 9.9) :** Injection de commande dans **Microsoft 365 Copilot**.
*   **CVE-2026-85878 (CVSS 9.9) :** Autorisation incorrecte dans **Azure Database for PostgreSQL**.
*   **CVE-2026-87701 (CVSS 9.6) :** Problème de neutralisation dans **Azure Cosmos DB**.
*   **CVE-2026-85921 (CVSS 8.2) :** *Double free* dans le noyau sécurisé Windows (Windows 11 26H1).
*   **CVE-2026-62721 (CVSS 7.8) :** Contrôle d'accès insuffisant dans le service d'alimentation en mode utilisateur (UMPS).

**Recommandations :**
*   Pour les services cloud (Azure, Copilot, Cosmos DB, PostgreSQL) : Aucune action n'est nécessaire, les correctifs sont déjà déployés côté serveur.
*   Pour les systèmes Windows 11 (version 26H1) : Appliquer la mise à jour cumulative de septembre 2026 (**KB5129194**) pour corriger les vulnérabilités locales.

---
[Source](https://thehackernews.com/2026/09/microsoft-patches-cvss-100-azure-ai.html){:target="_blank"}
