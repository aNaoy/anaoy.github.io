---
title: 'New critical Exim mailer flaw allows remote code execution'
date: 2026-05-14
permalink: /posts/2026/05/14/new-critical-exim-mailer-flaw-allows-remote-code-execution/
tags:
- veille-cyber
- bleepingcomp
---
# Vulnérabilité critique d'exécution de code à distance dans Exim

Une faille de sécurité critique a été découverte dans le serveur de messagerie (MTA) Exim, permettant à un attaquant non authentifié d'exécuter du code arbitraire sur les systèmes vulnérables.

### Points clés
* **Nature de la faille :** Une vulnérabilité de type *Use-After-Free* (UAF) survient lors de l'arrêt d'une connexion TLS pendant le traitement du trafic SMTP "BDAT". Le système continue d'utiliser des références obsolètes, permettant l'écriture dans une zone mémoire libérée.
* **Impact :** Les attaquants peuvent exécuter des commandes, accéder aux données et aux e-mails, voire se déplacer latéralement dans le réseau selon les privilèges du serveur.
* **Contexte :** La vulnérabilité a été identifiée lors d'un test comparatif entre un système d'IA autonome et un chercheur humain assisté par LLM, soulignant l'efficacité croissante des outils d'IA dans l'analyse de code complexe.

### Vulnérabilité
* **CVE-2026-45185**
* **Versions impactées :** Exim 4.97 à 4.99.2 compilés avec la bibliothèque **GnuTLS** et ayant les options STARTTLS et CHUNKING activées.
* **Note :** Les installations utilisant OpenSSL ne sont pas affectées.

### Recommandations
* **Mise à jour immédiate :** Appliquer la mise à jour vers la version **Exim 4.99.3**, qui corrige officiellement cette vulnérabilité.
* **Gestion des paquets :** Les utilisateurs de distributions Linux (notamment Debian et Ubuntu) doivent surveiller et appliquer les correctifs via leur gestionnaire de paquets officiel dès qu'ils sont disponibles.

---
[Source](https://www.bleepingcomputer.com/news/security/new-critical-exim-mailer-flaw-allows-remote-code-execution/){:target="_blank"}
