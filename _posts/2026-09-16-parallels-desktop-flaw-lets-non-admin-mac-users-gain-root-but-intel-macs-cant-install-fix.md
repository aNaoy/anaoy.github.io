---
title: 'Parallels Desktop Flaw Lets Non-Admin Mac Users Gain Root, but Intel Macs Cant Install Fix'
date: 2026-09-16
permalink: /posts/2026/09/16/parallels-desktop-flaw-lets-non-admin-mac-users-gain-root-but-intel-macs-cant-install-fix/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité d'élévation de privilèges dans Parallels Desktop

Une faille de sécurité critique, identifiée sous le nom **CVE-2026-90894**, permet à un utilisateur local non privilégié d'exécuter du code avec les droits **root** sur les systèmes macOS utilisant Parallels Desktop. Cette vulnérabilité, baptisée « ParaShells », exploite une mauvaise gestion des arguments dans le service `prl_disp_service`, qui s'exécute avec les privilèges les plus élevés du système.

**Points clés :**
* **Mécanisme :** L'attaque exploite une injection d'arguments via la commande `tar` lors de l'extraction de machines virtuelles. Le socket du service `prl_disp_service` étant accessible en écriture par tout utilisateur local, un attaquant peut manipuler le processus pour exécuter des commandes arbitraires en tant que root.
* **Impact :** Un utilisateur sans droits d'administration peut prendre le contrôle total de la machine hôte.
* **Portée :** La faille concerne les versions antérieures à la version 27.0.0.
* **Risque majeur :** Les utilisateurs de Mac basés sur des processeurs **Intel** sont particulièrement exposés, car la version 27, qui corrige la faille, est exclusivement réservée aux Mac équipés de puces Apple Silicon. Aucune solution de correction n'est actuellement confirmée pour la branche 26.x utilisée par les machines Intel.

**Vulnérabilité :**
* **CVE-2026-90894** (Score : 7.8/10)

**Recommandations :**
* **Mise à jour :** Pour les utilisateurs sur Apple Silicon, migrer immédiatement vers Parallels Desktop 27.0.1 ou version ultérieure.
* **Audit de sécurité :** Vérifier l'exposition via les commandes :
    * `defaults read "/Applications/Parallels Desktop.app/Contents/Info" CFBundleShortVersionString` (vérification de la version).
    * `ls -l /var/run/prl_disp_service.socket` (si les droits affichent `srwxrwxrwx`, le système est exposé).
* **Atténuation (pour les machines Intel ou non mises à jour) :**
    * Restreindre strictement les accès utilisateurs aux sessions locales sur les machines équipées de Parallels Desktop.
    * Inventorier l'ensemble du parc informatique pour identifier les instances vulnérables.
    * Être vigilant face aux scripts malveillants (npm, Homebrew) pouvant être exécutés par des utilisateurs locaux, car ils constituent le vecteur d'entrée principal pour cette exploitation.

---
[Source](https://thehackernews.com/2026/09/parallels-desktop-flaw-lets-non-admin.html){:target="_blank"}
