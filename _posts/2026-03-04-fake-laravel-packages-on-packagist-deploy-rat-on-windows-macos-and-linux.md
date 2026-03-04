---
title: 'Fake Laravel Packages on Packagist Deploy RAT on Windows, macOS, and Linux'
date: 2026-03-04
permalink: /posts/2026/03/04/fake-laravel-packages-on-packagist-deploy-rat-on-windows-macos-and-linux/
tags:
- veille-cyber
- hackernews
---
## Cheval de Troie via des Packages Laravel Malveillants

Des chercheurs en cybersécurité ont identifié des paquets PHP sur la plateforme Packagist, se présentant comme des utilitaires pour le framework Laravel, qui déploient en réalité un cheval de Troie d'accès à distance (RAT). Ce logiciel malveillant est opérationnel sur Windows, macOS et Linux.

Les paquets concernés sont :
*   `nhattuanbl/lara-helper`
*   `nhattuanbl/simple-queue`
*   `nhattuanbl/lara-swagger`

Le paquet `nhattuanbl/lara-swagger`, bien que n'intégrant pas directement le code malveillant, déclare `nhattuanbl/lara-helper` comme dépendance, entraînant ainsi l'installation du RAT. Ces paquets restent téléchargeables.

Les paquets `lara-helper` et `simple-queue` contiennent un fichier `src/helper.php` qui utilise diverses techniques d'obfuscation pour échapper à l'analyse statique. Une fois activé, le RAT établit une connexion avec un serveur de commande et de contrôle (C2) à l'adresse `helper.leuleu[.]net:2096`. Il transmet des informations système et attend des commandes pour exécution.

**Vulnérabilités et Fonctionnalités du RAT :**

*   **Exécution de commandes système :** Le RAT peut exécuter des commandes shell natives (`cmd`, `powershell`, commandes en arrière-plan). Pour contourner les mesures de sécurité, il recherche la première fonction disponible parmi `popen`, `proc_open`, `exec`, `shell_exec`, `system`, `passthru`.
*   **Collecte d'informations :** Envoi de données de reconnaissance système au serveur C2.
*   **Manipulation de fichiers :** Lecture et écriture de fichiers arbitraires sur le système compromis, avec possibilité de définir des permissions de lecture, écriture et exécution pour tous les utilisateurs.
*   **Capture d'écran :** Possibilité de prendre des captures d'écran.
*   **Persistance :** Le RAT tente de se reconnecter au serveur C2 toutes les 15 secondes en cas d'échec.
*   **Accès aux informations sensibles :** S'exécutant dans le même processus que l'application web, il a accès aux mêmes permissions système et variables d'environnement, y compris les identifiants de base de données, les clés API et le contenu du fichier `.env`.

**Recommandations :**

*   Les utilisateurs ayant installé les paquets `lara-helper` ou `simple-queue` doivent considérer leurs systèmes comme compromis.
*   Il est impératif de supprimer ces paquets.
*   Faire pivoter tous les secrets (mots de passe, clés API, etc.) accessibles depuis l'environnement de l'application.
*   Auditer le trafic sortant vers le serveur C2 identifié.
*   Les auteurs de la campagne ont également publié d'autres paquets apparemment propres (`nhattuanbl/lara-media`, `nhattuanbl/snooze`, `nhattuanbl/syslog`) dans le but de gagner en crédibilité et d'attirer les utilisateurs vers les versions malveillantes.

---
[Source](https://thehackernews.com/2026/03/fake-laravel-packages-on-packagist.html){:target="_blank"}
