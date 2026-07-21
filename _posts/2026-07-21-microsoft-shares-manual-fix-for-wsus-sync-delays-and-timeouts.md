---
title: 'Microsoft shares manual fix for WSUS sync delays and timeouts'
date: 2026-07-21
permalink: /posts/2026/07/21/microsoft-shares-manual-fix-for-wsus-sync-delays-and-timeouts/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des délais de synchronisation et timeouts sur WSUS

Des lenteurs et des échecs de synchronisation affectent les serveurs Windows Server Update Services (WSUS), empêchant le déploiement correct des mises à jour Windows sur les parcs informatiques (Windows 10 et versions ultérieures, Windows Server 2012 et versions ultérieures). Ce problème est causé par une accumulation excessive de métadonnées de publication dans la base de données.

**Points clés :**
*   **Cause :** Accumulation de métadonnées inutiles dans la base de données SUSDB.
*   **Impact :** Échecs ou dépassements de délai (timeouts) lors des opérations de synchronisation WSUS et via Configuration Manager.
*   **Statut :** Microsoft a déployé un correctif côté serveur pour les nouvelles installations, mais une intervention manuelle est requise pour les infrastructures existantes.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, il s'agit d'un problème de performance et de maintenance logicielle plutôt que d'une faille de sécurité exploitable.

**Recommandations pour les administrateurs :**
Pour restaurer le fonctionnement normal des serveurs existants, les étapes suivantes sont nécessaires :
1.  **Sauvegarde :** Effectuer une sauvegarde complète de toutes les bases de données SUSDB.
2.  **Nettoyage SQL :** Exécuter une requête de nettoyage spécifique via SQL Management Studio sur toutes les bases (y compris les réplicas).
3.  **Configuration :** Rétablir la valeur `MaxXMLPerRequest` à son réglage par défaut.
4.  **Optimisation finale :** 
    *   Réindexer la base SUSDB.
    *   Lancer l'assistant de nettoyage du serveur WSUS (*WSUS Server Cleanup Wizard*).
    *   Redémarrer IIS (`iisreset`) ou recycler le pool d'applications `WsusPool` pour vider le cache.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-manual-fix-for-wsus-sync-delays-and-timeouts/){:target="_blank"}
