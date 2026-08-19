---
title: 'Microsoft Links 30+ Rotating Domains to MacSync Stealer Infrastructure'
date: 2026-08-19
permalink: /posts/2026/08/19/microsoft-links-30-rotating-domains-to-macsync-stealer-infrastructure/
tags:
- veille-cyber
- hackernews
---
### Analyse des infrastructures du logiciel espion MacSync

Microsoft a identifié plus de 30 domaines web liés à **MacSync Stealer**, un logiciel malveillant conçu pour exfiltrer des données sur macOS. L'infrastructure des attaquants repose sur une rotation constante des serveurs, mais conserve des comportements réseau et processus cohérents permettant de les identifier.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de l'ingénierie sociale de type "ClickFix", incitant les victimes à exécuter des commandes dans une session Terminal (`zsh`).
*   **Mode opératoire :** Le malware utilise `curl` pour récupérer des charges utiles, les décode via `Base64`/`gunzip`, puis emploie `osascript` pour exécuter des scripts AppleScript malveillants.
*   **Objectifs :** Exfiltration massive de données sensibles, incluant le Trousseau d'accès (Keychain), les cookies/identifiants de navigateurs, les clés SSH, les configurations AWS/Kubernetes et les Notes Apple.
*   **Exfiltration :** Les données sont compressées dans des archives temporaires (`/tmp/osalogging.zip`), segmentées en fragments, puis envoyées via des requêtes HTTP PUT avec des paramètres récurrents (`upload_id`, `chunk_index`).

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exploitation de fonctionnalités légitimes du système (Living-off-the-land) :
*   **Abus des utilitaires système :** Utilisation détournée de `zsh`, `curl`, `osascript` et des outils de compression natifs.
*   **Ingénierie sociale :** Incitation de l'utilisateur à outrepasser les mesures de sécurité en copiant-collant manuellement des commandes malveillantes dans le terminal.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à ne jamais copier ni exécuter des commandes provenant de sources non fiables (sites web, messageries, support technique).
*   **Surveillance comportementale :** Détecter les sessions Terminal suspectes (lancement de `curl` suivi d'une activité AppleScript et d'un accès aux magasins d'identifiants).
*   **Analyse réseau :** Surveiller les requêtes HTTP PUT suspectes contenant des paramètres de découpage (chunks) et les chemins d'URL récurrents (`/curl/`, `/gate`, `/dynamic`).
*   **Mise à jour :** Utiliser les protections intégrées des versions récentes de macOS (Terminal paste protection, blocage de commandes via le presse-papier et analyse automatique des scripts par XProtect).

---
[Source](https://thehackernews.com/2026/08/microsoft-links-30-rotating-domains-to.html){:target="_blank"}
