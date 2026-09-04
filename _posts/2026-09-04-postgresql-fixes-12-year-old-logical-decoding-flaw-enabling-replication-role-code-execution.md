---
title: 'PostgreSQL Fixes 12-Year-Old Logical Decoding Flaw Enabling Replication-Role Code Execution'
date: 2026-09-04
permalink: /posts/2026/09/04/postgresql-fixes-12-year-old-logical-decoding-flaw-enabling-replication-role-code-execution/
tags:
- veille-cyber
- hackernews
---
### PostGREShell : Vulnérabilité d'exécution de code dans PostgreSQL

Une faille critique, nommée « PostGREShell », affecte le mécanisme de décodage logique de PostgreSQL depuis 2014. Elle permet à un utilisateur disposant du rôle `REPLICATION` d'exécuter du code arbitraire avec les privilèges du processus serveur.

**Points clés :**
*   **Vulnérabilité :** L'absence de restriction sur le chargement des bibliothèques externes lors de la création d'un slot de réplication permet d'injecter des chemins de fichiers malveillants.
*   **Impact :** Un attaquant peut obtenir les droits de superutilisateur et établir une persistance sur le serveur.
*   **Vecteurs :** Exploitation possible via le chargement de bibliothèques distantes (SMB sur Windows, NFS sur Linux/macOS) ou locales si l'attaquant peut déposer des fichiers.

**Vulnérabilité identifiée :**
*   **CVE-2026-6471** (Score CVSS : 7.2)

**Recommandations :**
1.  **Mise à jour :** Appliquer les correctifs vers les versions 18.6, 17.11, 16.15, 15.19 ou 14.24.
2.  **Configuration :** Utiliser le nouveau paramètre `output_plugin_libraries` pour restreindre les bibliothèques autorisées. Avant la mise à jour, lister les plugins en usage via `SELECT DISTINCT plugin FROM pg_replication_slots`.
3.  **Durcissement :**
    *   Retirer l'attribut `REPLICATION` des comptes non essentiels.
    *   Restreindre les accès réseau dans `pg_hba.conf` aux adresses IP de confiance.
    *   Bloquer les ports sortants associés aux partages de fichiers (SMB/445, NFS/2049) depuis le serveur de base de données.
    *   Désactiver le montage automatique (`autofs`) si inutile.

---
[Source](https://thehackernews.com/2026/09/postgresql-fixes-12-year-old-logical.html){:target="_blank"}
