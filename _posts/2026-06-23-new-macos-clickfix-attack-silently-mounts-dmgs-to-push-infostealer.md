---
title: 'New macOS ClickFix attack silently mounts DMGs to push infostealer'
date: 2026-06-23
permalink: /posts/2026/06/23/new-macos-clickfix-attack-silently-mounts-dmgs-to-push-infostealer/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne ClickFix : Propagation furtive d'infostealers sur macOS

Une nouvelle campagne d'ingénierie sociale nommée « ClickFix » cible les utilisateurs de macOS pour installer le malware *Atomic macOS Stealer* (AMOS). La technique consiste à inciter les victimes à copier-coller une commande dans le Terminal sous prétexte de valider un CAPTCHA ou de corriger une erreur système.

**Points clés :**
*   **Automatisation malveillante :** La commande Terminal téléchargée via `curl` télécharge un fichier DMG, le monte silencieusement via `hdiutil` (sans apparition dans le Finder) et exécute automatiquement le logiciel malveillant contenu.
*   **Objectifs du malware :** L'infostealer dérobe des identifiants de navigateurs (Chrome, Firefox, etc.), des portefeuilles de cryptomonnaies, des données de messagerie (Telegram, Discord), des fichiers du Keychain, ainsi que des documents personnels (PDF, TXT).
*   **Technique d'exfiltration :** Les données récoltées sont compressées en fichier ZIP puis envoyées vers un serveur distant contrôlé par les attaquants.
*   **Persistance ciblée :** Le malware remplace des applications légitimes de gestion de cryptomonnaies (Ledger Live, Trezor Suite) par des versions corrompues.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est exploitée ; l'attaque repose sur l'abus de fonctionnalités natives de macOS (`Terminal`, `curl`, `hdiutil`) via l'ingénierie sociale.

**Recommandations :**
*   **Méfiance absolue :** Ne jamais exécuter de commandes fournies par un site web, particulièrement pour des vérifications de type CAPTCHA, des corrections d'erreurs ou des procédures de dépannage.
*   **Vérification des commandes :** Si l'utilité d'une commande saisie dans le Terminal n'est pas parfaitement comprise, ne l'exécutez en aucun cas.
*   **Sensibilisation :** Informer les utilisateurs sur le fait que le système macOS ne nécessite jamais l'utilisation manuelle du Terminal pour valider une identité ou réparer une navigation web.

---
[Source](https://www.bleepingcomputer.com/news/security/new-macos-clickfix-attack-silently-mounts-dmgs-to-push-infostealer/){:target="_blank"}
