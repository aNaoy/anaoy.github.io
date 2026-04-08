---
title: 'New macOS stealer campaign uses Script Editor in ClickFix attack'
date: 2026-04-08
permalink: /posts/2026/04/08/new-macos-stealer-campaign-uses-script-editor-in-clickfix-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Nouvelle campagne de vol de données sur macOS via « ClickFix »

Une nouvelle campagne malveillante utilise une variante de l'attaque « ClickFix » pour déployer le logiciel espion **Atomic Stealer (AMOS)** sur macOS. Au lieu d'utiliser le Terminal, les attaquants détournent l'application **Script Editor** (Éditeur de scripts), native et approuvée par Apple, pour exécuter des commandes à l'insu de l'utilisateur.

**Fonctionnement de l'attaque**
*   **Vecteur d'infection :** Des sites web frauduleux imitent des guides officiels d'Apple (ex: nettoyage de disque).
*   **Exploitation :** La page utilise le protocole `applescript://` pour forcer l'ouverture de l'application « Éditeur de scripts » avec un code pré-rempli.
*   **Exécution :** Le script télécharge et exécute en mémoire une charge utile malveillante via `curl | zsh`, laquelle supprime les attributs de sécurité (`xattr -c`) avant de lancer le binaire Atomic Stealer.

**Points clés et risques**
*   **Cible :** Vol de données sensibles incluant le trousseau d'accès (Keychain), les mots de passe, les cookies, les données de saisie automatique et les portefeuilles de cryptomonnaies.
*   **Persistance :** Atomic Stealer intègre des fonctionnalités de porte dérobée permettant aux attaquants de conserver un accès permanent à la machine.
*   **Contournement :** Cette méthode cherche à éviter les nouvelles protections mises en place par Apple dans macOS Sequoia pour contrer les attaques directes via le Terminal.

**Vulnérabilités**
*   Pas de CVE spécifique identifiée : il s'agit d'un abus d'ingénierie sociale détournant des fonctionnalités légitimes du système.

**Recommandations**
*   **Vigilance accrue :** Ne jamais accepter l'ouverture d'un script via l'« Éditeur de scripts » provenant d'un site web inconnu.
*   **Source officielle :** Pour toute manipulation système ou dépannage, utilisez exclusivement la documentation officielle fournie par le support Apple.
*   **Méfiance :** Considérez toute invite système déclenchée par une interaction web comme suspecte si elle n'a pas été explicitement sollicitée par une procédure de maintenance connue.

---
[Source](https://www.bleepingcomputer.com/news/security/new-macos-stealer-campaign-uses-script-editor-in-clickfix-attack/){:target="_blank"}
