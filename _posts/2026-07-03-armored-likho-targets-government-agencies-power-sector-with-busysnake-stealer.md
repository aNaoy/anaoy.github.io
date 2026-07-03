---
title: 'Armored Likho Targets Government Agencies, Power Sector with BusySnake Stealer'
date: 2026-07-03
permalink: /posts/2026/07/03/armored-likho-targets-government-agencies-power-sector-with-busysnake-stealer/
tags:
- veille-cyber
- hackernews
---
### Menace cybernétique : Armored Likho et le déploiement de BusySnake Stealer

Le groupe de menace « Armored Likho » (potentiellement lié au cluster « Eagle Werewolf ») cible des agences gouvernementales et le secteur de l'énergie en Russie, au Brésil et au Kazakhstan. Ce groupe combine espionnage industriel et objectifs financiers en utilisant des outils sophistiqués et modulaires, incluant désormais le logiciel malveillant « BusySnake Stealer ».

**Points clés :**
*   **Vecteurs d'attaque :** Utilisation d'e-mails de spear-phishing (leurres administratifs) contenant des archives RAR ou des raccourcis Windows (.LNK) malveillants.
*   **Techniques d'évasion :** Utilisation de scripts VBScript pour effacer les traces, exécution en arrière-plan (.PYW) et déchiffrement dynamique du code en mémoire pour contrer l'analyse statique.
*   **Capacités de BusySnake :** Vol de cookies, de mots de passe, de captures d'écran, de données Telegram, de portefeuilles de cryptomonnaie et établissement de tunnels SSH inversés via `Go2Tunnel` ou `RustDesk`.
*   **Modernisation :** Utilisation probable d'outils d'IA pour générer des loaders et intégration directe de fonctionnalités de tunneling au sein du stealer.

**Vulnérabilité exploitée :**
*   **CVE-2025-9491 :** Une faille de type exécution de code à distance (RCE) liée au traitement des fichiers raccourcis (.LNK) par Windows.

**Recommandations :**
*   **Mise à jour système :** S'assurer que tous les correctifs de sécurité Microsoft (notamment ceux post-novembre 2025) sont appliqués pour corriger la vulnérabilité LNK.
*   **Filtrage des e-mails :** Renforcer la vigilance face aux e-mails contenant des pièces jointes inhabituelles ou des raccourcis.
*   **Restriction logicielle :** Limiter l'exécution de scripts PowerShell et VBScript via des politiques de groupe (GPO) pour les utilisateurs non administratifs.
*   **Surveillance réseau :** Détecter et bloquer les communications suspectes vers des serveurs de commande et contrôle (C2) et surveiller l'installation non autorisée d'outils comme RustDesk ou Go2Tunnel.

---
[Source](https://thehackernews.com/2026/07/armored-likho-targets-government.html){:target="_blank"}
