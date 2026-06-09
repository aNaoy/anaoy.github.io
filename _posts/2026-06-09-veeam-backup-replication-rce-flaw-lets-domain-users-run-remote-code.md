---
title: 'Veeam Backup & Replication RCE Flaw Lets Domain Users Run Remote Code'
date: 2026-06-09
permalink: /posts/2026/06/09/veeam-backup-replication-rce-flaw-lets-domain-users-run-remote-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de RCE dans Veeam Backup & Replication

Une faille de sécurité critique, identifiée sous la référence **CVE-2026-44963** (score CVSS de 9.4/10), affecte le logiciel Veeam Backup & Replication. Cette vulnérabilité permet à tout utilisateur authentifié du domaine d'exécuter du code à distance sur le serveur de sauvegarde.

**Points clés :**
*   **Impact :** L'exploitation réussie donne un accès non autorisé permettant l'exécution de code à distance (RCE).
*   **Versions vulnérables :** Veeam Backup & Replication 12.3.2.4465 et toutes les versions antérieures de la branche 12.
*   **Versions non affectées :** Les versions 13.x ne sont pas vulnérables en raison de changements structurels.
*   **Contexte :** Compte tenu de l'historique d'exploitation des logiciels Veeam par des groupes de ransomwares, une correction rapide est impérative.

**Vulnérabilité :**
*   **CVE-2026-44963 :** Permet une exécution de code à distance (RCE) par un utilisateur du domaine authentifié.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer le correctif en effectuant la mise à jour vers la version **12.3.2.4854** ou supérieure.
*   **Surveillance :** Maintenir une veille active sur les correctifs de sécurité fournis par l'éditeur, étant donné la criticité élevée de ce type d'outil pour la résilience des infrastructures.

---
[Source](https://thehackernews.com/2026/06/veeam-backup-replication-rce-flaw-lets.html){:target="_blank"}
