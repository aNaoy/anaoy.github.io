---
title: 'Vulnérabilité dans F5 BIG-IP Access Policy Manager (31 mars 2026)'
date: 2026-03-31
permalink: /posts/2026/03/31/vulnerabilite-dans-f5-big-ip-access-policy-manager-31-mars-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilité critique exploitée dans F5 BIG-IP APM

Une faille de sécurité critique affecte le module **BIG-IP Access Policy Manager (APM)** de F5, permettant à un attaquant non authentifié d'exécuter du code arbitraire à distance. Cette vulnérabilité fait actuellement l'objet d'une exploitation active.

**Vulnérabilité**
*   **CVE-2025-53521** : Exécution de code à distance (RCE).

**Systèmes affectés**
Les versions suivantes sont vulnérables si elles sont antérieures aux correctifs indiqués :
*   15.1.x < 15.1.10.8
*   16.1.x < 16.1.6.1
*   17.1.x < 17.1.3
*   17.5.x < 17.5.1.3

**Recommandations et détection**
*   **Mise à jour :** Appliquer immédiatement les correctifs fournis par l'éditeur (cf. Bulletin F5 K000156741).
*   **Recherche de compromission (IoC) :**
    *   **Système de fichiers :** Rechercher des fichiers suspects (`/run/bigtlog.pipe`, `/run/bigstart.ltm`) ou des anomalies sur les exécutables `/usr/bin/umount` et `/usr/sbin/httpd` (tailles, dates ou condensats modifiés).
    *   **Journaux :** Analyser les logs (`restjavad-audit`, `audit.log`, `/var/log/audit`) pour identifier des requêtes iControl REST suspectes, des tentatives de désactivation de SELinux ou des exécutions de commandes `bash` non autorisées par l'utilisateur `f5hubblelcdadmin`.
    *   **Vérification système :** Exécuter l'outil d'intégrité `sys-eicheck` pour détecter des erreurs de conformité sur les exécutables critiques et utiliser `lsof -n` pour vérifier la présence du pipe malveillant.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-004/){:target="_blank"}
