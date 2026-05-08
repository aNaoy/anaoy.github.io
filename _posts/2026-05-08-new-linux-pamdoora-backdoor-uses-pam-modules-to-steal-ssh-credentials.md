---
title: 'New Linux PamDOORa Backdoor Uses PAM Modules to Steal SSH Credentials'
date: 2026-05-08
permalink: /posts/2026/05/08/new-linux-pamdoora-backdoor-uses-pam-modules-to-steal-ssh-credentials/
tags:
- veille-cyber
- hackernews
---
### PamDOORa : Un nouveau backdoor persistant pour systèmes Linux

**Points clés**
* **Nature de la menace :** PamDOORa est un logiciel malveillant de type "backdoor" conçu sous forme de module PAM (Pluggable Authentication Module) pour Linux (x86_64).
* **Vecteur d'attaque :** Vendu sur des forums cybercriminels, il nécessite un accès root préalable au système pour être installé.
* **Fonctionnalités :** 
    * Accès SSH persistant via un "mot de passe magique" associé à un port TCP spécifique.
    * Vol d'identifiants en clair des utilisateurs légitimes.
    * Capacités anti-forensiques incluant la falsification des journaux d'authentification pour masquer toute activité malveillante.
* **Complexité :** Contrairement aux scripts de preuve de concept classiques, cet outil est présenté comme un logiciel de qualité professionnelle, incluant des mécanismes d'anti-débogage et une architecture modulaire.

**Vulnérabilités associées**
* Aucune CVE spécifique n'est associée à cet outil, car il s'agit d'une **exploitation malveillante de l'architecture PAM**.
* Le risque repose sur la capacité des attaquants à manipuler la configuration du système (fichiers de configuration PAM) une fois qu'ils ont obtenu des privilèges root. L'utilisation du module `pam_exec` est notamment citée comme un vecteur permettant l'exécution de commandes arbitraires.

**Recommandations**
* **Surveillance des configurations :** Auditer régulièrement les fichiers de configuration PAM (`/etc/pam.d/`) pour détecter toute modification non autorisée ou l'ajout de modules suspects.
* **Gestion des privilèges :** Restreindre strictement l'accès root sur les systèmes Linux et surveiller l'élévation de privilèges, car le déploiement de ce backdoor nécessite des droits d'administration.
* **Monitoring des journaux :** Mettre en place une journalisation centralisée et immuable (SIEM) pour détecter d'éventuelles tentatives de falsification ou de suppression de logs par des attaquants.
* **Authentification forte :** Bien que PAM gère les méthodes d'authentification, le renforcement de l'accès SSH via des clés robustes et la désactivation des mots de passe en clair restent des mesures de sécurité essentielles.

---
[Source](https://thehackernews.com/2026/05/new-linux-pamdoora-backdoor-uses-pam.html){:target="_blank"}
