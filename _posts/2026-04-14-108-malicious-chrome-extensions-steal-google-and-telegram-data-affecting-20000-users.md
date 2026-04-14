---
title: '108 Malicious Chrome Extensions Steal Google and Telegram Data, Affecting 20,000 Users'
date: 2026-04-14
permalink: /posts/2026/04/14/108-malicious-chrome-extensions-steal-google-and-telegram-data-affecting-20000-users/
tags:
- veille-cyber
- hackernews
---
### Vague de malwares : 108 extensions Chrome dérobent des données sensibles

Une campagne malveillante a été identifiée sur le Chrome Web Store, impliquant 108 extensions frauduleuses ayant cumulé 20 000 installations. Ces outils, se faisant passer pour des utilitaires (jeux, outils de traduction ou clients Telegram), communiquent tous avec une infrastructure de commande et de contrôle (C2) unique pour exfiltrer des données et injecter du code malveillant dans le navigateur.

**Points clés :**
*   **Objectifs :** Vol d'identifiants Google, détournement de sessions Telegram (exfiltration toutes les 15 secondes), injection de publicités et de scripts arbitraires, et contournement des protections web.
*   **Méthodes :** Utilisation de l'API `declarativeNetRequest` de Chrome pour supprimer les en-têtes de sécurité (CSP, CORS) sur des sites comme YouTube ou TikTok afin de faciliter l'injection de contenu.
*   **Origine :** Les extensions sont distribuées par cinq entités distinctes (Yana Project, GameGen, SideGames, Rodeo Games, InterAlt) et contiennent des commentaires en russe dans leur code source.

**Vulnérabilités et vecteurs d'attaque :**
*   **Vol d'OAuth2 :** Capture des jetons d'identité Google lors de l'utilisation des boutons de connexion.
*   **Détournement de session :** Vol des jetons `user_auth` de Telegram Web pour permettre aux attaquants de prendre le contrôle des sessions des victimes.
*   **Backdoor universelle :** 45 extensions intègrent une porte dérobée forçant l'ouverture d'URLs arbitraires au démarrage du navigateur.
*   *Note : Aucune CVE spécifique n'est mentionnée, il s'agit d'un usage malveillant détourné des fonctionnalités natives des extensions Chrome.*

**Recommandations :**
*   **Suppression immédiate :** Désinstaller sans délai toute extension suspecte.
*   **Réinitialisation des accès :** Déconnecter toutes les sessions actives de Telegram Web via l'application mobile Telegram pour invalider les jetons potentiellement compromis.
*   **Vigilance :** Vérifier régulièrement les permissions accordées aux extensions installées et limiter leur nombre au strict nécessaire.

---
[Source](https://thehackernews.com/2026/04/108-malicious-chrome-extensions-steal.html){:target="_blank"}
