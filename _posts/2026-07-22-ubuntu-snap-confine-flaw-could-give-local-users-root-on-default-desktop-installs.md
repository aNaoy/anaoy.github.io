---
title: 'Ubuntu snap-confine Flaw Could Give Local Users Root on Default Desktop Installs'
date: 2026-07-22
permalink: /posts/2026/07/22/ubuntu-snap-confine-flaw-could-give-local-users-root-on-default-desktop-installs/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'élévation de privilèges dans Ubuntu (snap-confine)

Une faille de sécurité critique a été découverte dans `snap-confine`, l'outil utilisé par `snapd` pour isoler les applications sous Ubuntu. Cette vulnérabilité permet à un utilisateur local non privilégié d'obtenir les droits `root` et de prendre le contrôle total du système.

**Points clés :**
*   **Nature du problème :** Une condition de concurrence (*race condition*) lors de l'initialisation du bac à sable (*sandbox*) permet de manipuler les permissions de fichiers temporaires avant que la propriété ne soit transférée à l'utilisateur root.
*   **Vecteur d'attaque :** L'attaquant utilise des systèmes de fichiers FUSE et des liens symboliques pour contourner l'isolation du bac à sable et injecter des règles malveillantes (notamment dans `/run/udev/rules.d/`), forçant `systemd-udevd` à exécuter des commandes avec les privilèges élevés.
*   **Impact :** Élévation de privilèges locale (LPE) sur les installations par défaut d'Ubuntu Desktop (versions 24.04, 25.10 et 26.04).

**Vulnérabilité identifiée :**
*   **CVE-2026-8933** (Score CVSS : 7.8)

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les dernières mises à jour de `snapd` fournies par Canonical dès que possible.
*   **Vérification :** Ne pas se fier uniquement à la version de la distribution ; les administrateurs doivent vérifier explicitement la version installée de `snapd` pour confirmer que le correctif est bien actif.

---
[Source](https://thehackernews.com/2026/07/ubuntu-snap-confine-flaw-could-give.html){:target="_blank"}
