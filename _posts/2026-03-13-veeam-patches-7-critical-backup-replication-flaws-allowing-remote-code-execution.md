---
title: 'Veeam Patches 7 Critical Backup & Replication Flaws Allowing Remote Code Execution'
date: 2026-03-13
permalink: /posts/2026/03/13/veeam-patches-7-critical-backup-replication-flaws-allowing-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Veeam Backup & Replication

Veeam a publié des mises à jour correctives pour remédier à sept vulnérabilités critiques affectant ses solutions *Backup & Replication*. Ces failles exposent les serveurs de sauvegarde à des risques d'exécution de code à distance (RCE), d'élévation de privilèges et de manipulation de fichiers.

**Points clés :**
* Les failles touchent les versions 12.3.2.4165 et antérieures, ainsi que certains composants de la version 13.
* Les attaquants ciblent fréquemment ces logiciels pour déployer des ransomwares.
* La rétro-ingénierie des correctifs par des acteurs malveillants est hautement probable, rendant une mise à jour immédiate indispensable.

**Vulnérabilités identifiées :**
* **CVE-2026-21666, CVE-2026-21667, CVE-2026-21669 (Score CVSS 9.9) :** Exécution de code à distance sur le serveur de sauvegarde par un utilisateur du domaine authentifié.
* **CVE-2026-21708 (Score CVSS 9.9) :** Exécution de code à distance via un « Backup Viewer ».
* **CVE-2026-21671 (Score CVSS 9.1) :** Exécution de code à distance dans les déploiements haute disponibilité (HA) par un administrateur de sauvegarde.
* **CVE-2026-21668 (Score CVSS 8.8) :** Contournement des restrictions et manipulation de fichiers sur un référentiel de sauvegarde.
* **CVE-2026-21672 (Score CVSS 8.8) :** Élévation de privilèges locale sur les serveurs Windows.

**Recommandations :**
* Mettre à jour vers la version **12.3.2.4465** pour corriger les versions 12.x.
* Mettre à jour vers la version **13.0.1.2067** pour les installations en version 13.
* Appliquer ces correctifs sans délai pour éviter l'exploitation des failles maintenant rendues publiques.

---
[Source](https://thehackernews.com/2026/03/veeam-patches-7-critical-backup.html){:target="_blank"}
