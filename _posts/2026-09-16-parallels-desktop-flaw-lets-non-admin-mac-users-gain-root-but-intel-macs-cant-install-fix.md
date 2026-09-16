---
title: 'Parallels Desktop Flaw Lets Non-Admin Mac Users Gain Root, but Intel Macs Cant Install Fix'
date: 2026-09-16
permalink: /posts/2026/09/16/parallels-desktop-flaw-lets-non-admin-mac-users-gain-root-but-intel-macs-cant-install-fix/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'élévation de privilèges dans Parallels Desktop

Une faille de sécurité identifiée dans Parallels Desktop permet à tout utilisateur local non privilégié d'exécuter du code avec les droits **root** sur macOS. Cette vulnérabilité, nommée "ParaShells", exploite une mauvaise gestion des arguments lors de l'extraction de machines virtuelles, permettant une injection de commande via l'utilitaire `tar`.

**Points clés :**
*   **Vecteur d'attaque :** Nécessite un accès local à la machine (exécution de code par un utilisateur standard).
*   **Mécanisme :** Le service `prl_disp_service` s'exécute avec les privilèges root et possède un socket accessible en écriture par tout utilisateur, facilitant l'injection de commandes malveillantes.
*   **Gravité :** Évaluée à 7.8/10 par JFrog.
*   **Situation critique pour Intel :** Le correctif est uniquement disponible dans la version 27, laquelle est incompatible avec les Mac équipés de processeurs Intel. Ces utilisateurs restent exposés sur la version 26.

**Vulnérabilité :**
*   **CVE-2026-90894**

**Recommandations :**
*   **Mise à jour :** Effectuer la mise à jour vers la version 27.0.1 ou ultérieure pour tous les Mac équipés de puces Apple Silicon.
*   **Audit de sécurité :** Vérifier l'exposition via les commandes suivantes :
    *   `defaults read "/Applications/Parallels Desktop.app/Contents/Info" CFBundleShortVersionString`
    *   `ls -l /var/run/prl_disp_service.socket` (si les permissions affichent `srwxrwxrwx`, le système est exposé).
*   **Mitigation :** En l'absence de correctif pour les versions Intel, restreindre strictement l'accès local aux comptes utilisateurs de confiance sur les machines concernées.
*   **Surveillance :** Garder à l'esprit qu'une mise à jour logicielle ne supprimera pas un accès root déjà établi par un attaquant ; une réinstallation propre du système peut être nécessaire en cas de compromission avérée.

---
[Source](https://thehackernews.com/2026/09/parallels-desktop-flaw-lets-non-admin.html){:target="_blank"}
