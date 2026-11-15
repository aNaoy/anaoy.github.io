---
title: 'Race Against the (Mac)hine: Local Privilege Escalation in Microsoft Defender for macOS'
date: 2026-11-15
permalink: /posts/2026/11/15/race-against-the-machine-local-privilege-escalation-in-microsoft-defender-for-macos/
tags:
- veille-cyber
- zerodaysfans
---
### Escalade de privilèges locale dans Microsoft Defender pour macOS

Cette recherche met en lumière des vulnérabilités critiques dans Microsoft Defender pour macOS, découlant de divergences d'implémentation par rapport à la version Windows. Bien que Microsoft ait corrigé des failles similaires sur Windows, les différences fondamentales dans la gestion des processus et des systèmes de fichiers sous macOS ont permis l'exploitation de variantes de ces vulnérabilités.

#### Points clés
*   **Architecture IPC vulnérable :** Microsoft Defender utilise des sockets `AF_UNIX` accessibles en écriture par n'importe quel utilisateur local (`0666`), déléguant la validation des pairs à un mécanisme de vérification sujet à une "course" (race condition).
*   **Contournement de validation :** L'utilisation combinée d'un PID figé au moment de la connexion et d'une résolution de chemin (`proc_pidpath`) vulnérable permet une attaque par réutilisation de PID via `execve()`. Un processus malveillant peut se faire passer pour un binaire signé par Microsoft après la connexion.
*   **Divergence macOS vs Windows :** Contrairement à Windows, les liens physiques (`hardlinks`) sous macOS ne nécessitent aucun droit d'accès au fichier cible, facilitant ainsi les attaques de type lecture arbitraire de fichiers.

#### Vulnérabilités
*   **CVE-2026-50657 (Lecture arbitraire de fichiers) :** L'opcode `get_diagnostic_files` n'est pas protégé par une vérification d'autorisation. En créant un lien physique vers un fichier sensible (ex: `/etc/kcpassword`) dans un répertoire log utilisateur, un attaquant force le processus root à lire et copier le contenu dans une archive ZIP accessible à l'utilisateur.
*   **CVE-2026-50658 (Escalade de privilèges - Écriture arbitraire) :** Une mauvaise gestion de l'objet `std::optional` dans le désérialiseur du socket privé permet d'ignorer totalement la vérification d'autorisation (`AuthorizationCopyRights`). Cela permet de restaurer des fichiers mis en quarantaine vers un emplacement arbitraire (ex: `/etc/crontab`), aboutissant à une exécution de code arbitraire en tant que root.

#### Recommandations
*   **Adopter XPC :** Migrer vers les mécanismes IPC natifs de macOS (XPC), qui supportent des APIs sécurisées comme `xpc_connection_get_audit_token` et `xpc_connection_set_peer_code_signing_requirement`, immunisées contre la réutilisation de PID.
*   **Renforcement des vérifications :** Ne jamais se reposer sur la simple vérification du chemin d'exécution (`proc_pidpath`) ; utiliser systématiquement les jetons d'audit (audit tokens) qui incluent un compteur de génération (`pidversion`).
*   **Sécurisation du système de fichiers :** Bloquer spécifiquement la création de liens physiques vers des cibles privilégiées ou restreindre les répertoires utilisés par le démon pour éviter les attaques par redirection, plutôt que de se limiter à la validation des liens symboliques.
*   **Audit de l'autorisation :** Découpler strictement le consentement de l'utilisateur (via *Authorization Services*) de l'authentification de l'appelant pour éviter les erreurs de logique métier.

---
[Source](https://spaceraccoon.dev/race-against-the-machine-defender-macos-lpe/){:target="_blank"}
