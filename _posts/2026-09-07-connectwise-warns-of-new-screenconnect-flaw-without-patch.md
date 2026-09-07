---
title: 'ConnectWise warns of new ScreenConnect flaw without patch'
date: 2026-09-07
permalink: /posts/2026/09/07/connectwise-warns-of-new-screenconnect-flaw-without-patch/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique identifiée sur ConnectWise ScreenConnect

ConnectWise a émis une alerte de sécurité concernant une faille affectant le transfert de fichiers dans sa plateforme d'accès distant ScreenConnect. Cette vulnérabilité, qui impacte à la fois les déploiements cloud et sur site, ne dispose pas encore d'identifiant CVE.

**Points clés :**
*   **Nature du risque :** La faille concerne la gestion du transfert de fichiers au sein des sessions d'accès distant, pouvant potentiellement être exploitée par des acteurs malveillants.
*   **Exposition :** Près de 6 000 instances de ScreenConnect sont actuellement accessibles via Internet, ce qui accroît la surface d'attaque.
*   **Contexte :** ScreenConnect est une cible privilégiée pour les groupes de ransomwares et les menaces persistantes avancées (APT), comme illustré par plusieurs incidents critiques répertoriés ces dernières années (notamment CVE-2024-1709, CVE-2025-3935 et CVE-2026-3564).

**Recommandations :**
En attendant la publication d'un correctif officiel prévue pour la fin de la semaine, les administrateurs informatiques sont invités à appliquer une mesure d'atténuation temporaire :
1.  Se connecter à la page d'administration de ScreenConnect.
2.  Accéder à la section **Administration > Sécurité > Rôles**.
3.  Modifier les rôles des utilisateurs pour accéder aux groupes de sessions.
4.  Dans la fenêtre des permissions, décocher l'autorisation `TransferFiles` (ou `TransferFilesInSession` pour les anciennes versions).
5.  Enregistrer les modifications pour chaque rôle utilisateur.

---
[Source](https://www.bleepingcomputer.com/news/security/connectwise-warns-of-new-screenconnect-flaw-without-patch/){:target="_blank"}
