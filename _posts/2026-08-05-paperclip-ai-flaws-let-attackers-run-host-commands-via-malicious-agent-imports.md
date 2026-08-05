---
title: 'Paperclip AI Flaws Let Attackers Run Host Commands via Malicious Agent Imports'
date: 2026-08-05
permalink: /posts/2026/08/05/paperclip-ai-flaws-let-attackers-run-host-commands-via-malicious-agent-imports/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Paperclip : Exécution de code via des agents malveillants

La plateforme open-source Paperclip, utilisée pour orchestrer des agents d'intelligence artificielle, est affectée par trois vulnérabilités majeures permettant l'exécution arbitraire de commandes sur les serveurs ou les postes des développeurs, ainsi que l'exfiltration de données sensibles.

**Points clés :**
*   **Vecteur d'attaque :** Le mécanisme de configuration des agents est interprété comme du code exécutable. Un attaquant peut injecter une configuration malveillante qui, une fois importée, est lancée par l'adaptateur de processus de Paperclip avec les privilèges du serveur.
*   **Défaut de confiance :** Les failles exploitent une gestion laxiste des droits d'accès, traitant indûment certaines requêtes réseau (localhost) ou nouveaux utilisateurs comme des administrateurs système.
*   **Complexité de versioning :** Il existe une confusion dans les étiquettes de version (v0.3.1 vs v2026.416.0), mais le code source tagué **v2026.416.0** contient bien les correctifs nécessaires.

**Vulnérabilités identifiées :**
*   **CVE-2026-41679 (Score CVSS 10.0) :** Permet à un utilisateur non authentifié d'enregistrer un compte, de s'auto-attribuer des droits d'administrateur et d'importer une configuration malveillante pour exécuter du code sur le serveur.
*   **GHSA-x8hx-rhr2-9rf7 (Score CVSS 9.6) :** Attaque par rebond DNS (DNS rebinding) permettant à un site web malveillant d'interagir avec une instance Paperclip locale (`local_trusted`) et d'exécuter des commandes sur la machine du développeur.
*   **GHSA-xfqj-r5qw-8g4j (Score CVSS 8.3) :** Défaut de contrôle d'accès sur plusieurs routes API permettant la fuite d'informations sensibles (données d'incidents, documentation interne, détails de déploiement).

**Recommandations :**
1.  **Mise à jour immédiate :** Mettre à jour vers la version **v2026.416.0** ou ultérieure.
2.  **Audit de configuration :** Revoir les paramètres de déploiement, notamment le mode d'enregistrement (open-signup) et les niveaux d'accès attribués aux instances locales.
3.  **Filtrage :** S'assurer que le garde-fou de validation des noms d'hôtes (hostname guard) est bien activé pour empêcher les attaques par rebond DNS, une mesure désormais incluse dans la version corrigée.

---
[Source](https://thehackernews.com/2026/08/paperclip-ai-flaws-let-attackers-run.html){:target="_blank"}
