---
title: 'New PHP Composer Flaws Enable Arbitrary Command Execution — Patches Released'
date: 2026-04-14
permalink: /posts/2026/04/14/new-php-composer-flaws-enable-arbitrary-command-execution-patches-released/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques d'exécution de code dans PHP Composer

Deux failles de sécurité critiques ont été découvertes dans Composer, le gestionnaire de paquets pour PHP. Ces vulnérabilités, liées au pilote Perforce VCS, permettent à un attaquant d'exécuter des commandes arbitraires sur le système de l'utilisateur.

**Points clés :**
* Les failles permettent une injection de commandes via une manipulation du fichier `composer.json` ou des références sources malveillantes.
* Le risque existe même si le logiciel Perforce VCS n'est pas installé sur la machine.
* Aucune preuve d'exploitation active n'a été détectée sur Packagist.org à ce jour.

**Vulnérabilités :**
* **CVE-2026-40176 (CVSS 7.8) :** Injection de commandes via une configuration de dépôt Perforce malveillante dans `composer.json`.
* **CVE-2026-40261 (CVSS 8.8) :** Injection de commandes par défaut d'échappement dans les références sources contenant des métacaractères shell.

**Versions affectées et correctifs :**
* Versions 2.3 à < 2.9.6 : Mettre à jour vers la version **2.9.6**.
* Versions 2.0 à < 2.2.27 : Mettre à jour vers la version **2.2.27**.

**Recommandations :**
* Mettre à jour Composer immédiatement.
* Vérifier systématiquement le contenu des fichiers `composer.json` provenant de sources tierces.
* N'utiliser que des dépôts de confiance et éviter l'utilisation de l'option `--prefer-dist`.
* La publication de métadonnées Perforce a été temporairement désactivée sur Packagist.org par mesure de précaution.

---
[Source](https://thehackernews.com/2026/04/new-php-composer-flaws-enable-arbitrary.html){:target="_blank"}
