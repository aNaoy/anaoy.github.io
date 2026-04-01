---
title: 'Claude AI finds Vim, Emacs RCE bugs that trigger on file open'
date: 2026-04-01
permalink: /posts/2026/04/01/claude-ai-finds-vim-emacs-rce-bugs-that-trigger-on-file-open/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques par exécution de code dans Vim et Emacs

Des recherches assistées par l'IA Claude ont permis d'identifier des failles d'exécution de code à distance (RCE) dans les éditeurs de texte Vim et GNU Emacs, déclenchables par la simple ouverture d'un fichier piégé.

**Points clés :**
* **Vim :** La faille réside dans la gestion des « modelines ». Un attaquant peut injecter du code malveillant dans un fichier qui, une fois ouvert, contourne les mesures de sécurité (sandbox) pour exécuter des commandes avec les privilèges de l'utilisateur.
* **GNU Emacs :** La vulnérabilité est liée à l'intégration du contrôle de version (vc-git). L'ouverture d'un fichier déclenche automatiquement des opérations Git qui lisent un fichier `.git/config` malveillant, permettant l'exécution arbitraire de commandes. Les mainteneurs d'Emacs rejettent la responsabilité sur Git.

**Vulnérabilités :**
* **Vim :** Affecte toutes les versions 9.2.0271 et antérieures. (Aucun identifiant CVE assigné).
* **GNU Emacs :** Problème de conception non corrigé lié à l'exécution automatique de `core.fsmonitor` via Git.

**Recommandations :**
* **Pour Vim :** Mettre à jour immédiatement vers la version **9.2.0272** ou supérieure, qui inclut le correctif officiel.
* **Pour GNU Emacs :** Faire preuve d'une extrême prudence lors de l'ouverture de fichiers provenant de sources inconnues ou téléchargés en ligne. Il est conseillé de bloquer explicitement l'option `core.fsmonitor` dans les configurations Git tant qu'une solution officielle n'est pas déployée par les éditeurs.

---
[Source](https://www.bleepingcomputer.com/news/security/claude-ai-finds-vim-emacs-rce-bugs-that-trigger-on-file-open/){:target="_blank"}
