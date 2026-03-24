---
title: 'Ghost Campaign Uses 7 npm Packages to Steal Crypto Wallets and Credentials'
date: 2026-03-24
permalink: /posts/2026/03/24/ghost-campaign-uses-7-npm-packages-to-steal-crypto-wallets-and-credentials/
tags:
- veille-cyber
- hackernews
---
### Campagne « Ghost » : Malwares npm et vol de données

Des chercheurs en cybersécurité ont identifié une campagne malveillante sophistiquée, baptisée « Ghost », utilisant des bibliothèques npm et des dépôts GitHub pour infecter les développeurs. Cette menace, qui partage des similitudes avec la campagne « GhostClaw », vise à dérober des portefeuilles de cryptomonnaies, des identifiants système, des clés SSH et des jetons d'outils de développement.

**Points clés :**
*   **Tactique d'ingénierie sociale :** Les attaquants publient des packages npm (ex: `react-performance-suite`, `ai-fast-auto-trader`) et des dépôts GitHub (parfois dotés d'une forte popularité) qui imitent des outils légitimes.
*   **Installation trompeuse :** Les scripts affichent de faux logs d'installation et des barres de progression factices pour instaurer la confiance.
*   **Escalade de privilèges :** Le malware simule une erreur de permission d'écriture, incitant la victime à saisir son mot de passe `sudo` ou administrateur.
*   **Charge utile (Payload) :** Une fois le mot de passe obtenu, le système déploie un cheval de Troie d'accès à distance (RAT) nommé **GhostLoader**.
*   **Infrastructure :** La communication avec le serveur de commande (C2) et l'exfiltration des données passent souvent par Telegram. Le modèle économique inclut également des redirections d'affiliation via des smart contracts sur la Binance Smart Chain (BSC).

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'une attaque par **empoisonnement de supply chain** (chaîne d'approvisionnement logicielle) exploitant la confiance des utilisateurs envers les dépôts open source et les processus d'installation nécessitant des privilèges élevés.

**Recommandations :**
*   **Vigilance sur les privilèges :** Ne jamais exécuter de scripts d'installation inconnus avec des droits `sudo` ou administrateur, surtout si le script demande un mot de passe pour des opérations de "configuration" suspectes.
*   **Audit des dépendances :** Vérifier systématiquement la réputation et le volume de téléchargements des packages npm avant leur intégration dans un projet.
*   **Analyse du code source :** Inspecter le contenu des fichiers `postinstall.js` ou des scripts shell associés dans les nouveaux dépôts avant exécution.
*   **Zero Trust :** Maintenir une posture de méfiance envers les outils provenant de sources non vérifiées, même s'ils semblent populaires ou bien documentés sur GitHub.

---
[Source](https://thehackernews.com/2026/03/ghost-campaign-uses-7-npm-packages-to.html){:target="_blank"}
