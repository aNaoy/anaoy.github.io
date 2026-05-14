---
title: 'Stealer Backdoor Found in 3 Node-IPC Versions Targeting Developer Secrets'
date: 2026-05-14
permalink: /posts/2026/05/14/stealer-backdoor-found-in-3-node-ipc-versions-targeting-developer-secrets/
tags:
- veille-cyber
- hackernews
---
### Compromission de la bibliothèque node-ipc : Vol de données sensibles via backdoor

Des chercheurs en cybersécurité ont identifié des versions malveillantes de la bibliothèque npm `node-ipc`, conçues pour dérober des secrets de développement et des identifiants cloud. Cette attaque par chaîne d'approvisionnement utilise une exécution immédiate de fonction (IIFE) pour contourner les mécanismes de sécurité classiques, sans nécessiter de scripts d'installation.

**Points clés :**
*   **Versions compromises :** `9.1.6`, `9.2.3` et `12.0.1`.
*   **Propagation :** Le code malveillant est injecté directement dans le fichier `node-ipc.cjs`, s'exécutant à chaque appel de la bibliothèque via `require()`.
*   **Techniques d'évasion :** Utilisation d'obfuscation lourde, contournement des serveurs DNS locaux en forçant l'utilisation de résolveurs publics (Google DNS), et ciblage précis par empreinte SHA-256 (pour la version `12.0.1`).
*   **Exfiltration :** Les données récoltées (clés SSH, tokens cloud, fichiers de configuration, historique shell) sont compressées et envoyées vers le domaine `sh.azurestaticprovider[.]net`.

**Vulnérabilités :**
Il n'existe pas de numéro CVE spécifique associé à cet incident pour le moment, car il s'agit d'une compromission de compte de mainteneur menant à l'insertion intentionnelle de code malveillant (Supply Chain Attack).

**Recommandations :**
1.  **Suppression et mise à jour :** Désinstaller immédiatement les versions compromises et réinstaller une version saine (`9.2.1` ou `12.0.0`).
2.  **Rotation des secrets :** Considérer tous les identifiants présents sur les machines ayant utilisé ces versions comme compromis. Procéder à une rotation immédiate des clés AWS, GCP, Azure, GitHub, Kubernetes, et autres tokens d'accès.
3.  **Audit :** Examiner les journaux de flux réseau pour détecter des connexions sortantes vers `sh.azurestaticprovider[.]net` et auditer les logs d'accès cloud pour toute activité inhabituelle liée aux identifiants exposés.
4.  **Blocage :** Bloquer tout trafic sortant vers le domaine C2 identifié au niveau du pare-feu ou du proxy.

---
[Source](https://thehackernews.com/2026/05/stealer-backdoor-found-in-3-node-ipc.html){:target="_blank"}
