---
title: '9-Year-Old Linux Kernel Flaw Enables Root Command Execution on Major Distros'
date: 2026-05-21
permalink: /posts/2026/05/21/9-year-old-linux-kernel-flaw-enables-root-command-execution-on-major-distros/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de privilèges dans le noyau Linux (CVE-2026-46333)

Une faille de sécurité vieille de neuf ans a été identifiée dans la fonction `__ptrace_may_access()` du noyau Linux (introduite en novembre 2016). Cette vulnérabilité permet à un utilisateur local non privilégié d'accéder à des fichiers sensibles et d'exécuter des commandes avec les droits "root".

**Points clés :**
*   **Impact :** Élévation locale de privilèges et divulgation d'informations sensibles (ex: `/etc/shadow`, clés privées SSH).
*   **Vecteurs d'exploitation :** Quatre exploits distincts ciblant `chage`, `ssh-keysign`, `pkexec` et `accounts-daemon`.
*   **Disponibilité :** Un code d'exploitation (PoC) est désormais public, rendant la menace immédiate pour les distributions majeures comme Debian, Fedora et Ubuntu.

**Vulnérabilité identifiée :**
*   **CVE-2026-46333** (Score CVSS : 5.5) – Surnommée *ssh-keysign-pwn*.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement les correctifs de noyau fournis par votre distribution Linux.
*   **Atténuation temporaire :** Si la mise à jour est impossible, augmenter la portée de la protection via la commande : `sysctl -w kernel.yama.ptrace_scope=2`.
*   **Audit de sécurité :** Sur les systèmes ayant potentiellement été exposés, procéder à une rotation des clés SSH hôtes et examiner les identifiants ou données administratives potentiellement compromis en mémoire.

---
[Source](https://thehackernews.com/2026/05/9-year-old-linux-kernel-flaw-enables.html){:target="_blank"}
