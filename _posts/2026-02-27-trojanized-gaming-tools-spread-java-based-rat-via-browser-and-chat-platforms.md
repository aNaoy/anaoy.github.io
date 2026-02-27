---
title: 'Trojanized Gaming Tools Spread Java-Based RAT via Browser and Chat Platforms'
date: 2026-02-27
permalink: /posts/2026/02/27/trojanized-gaming-tools-spread-java-based-rat-via-browser-and-chat-platforms/
tags:
- veille-cyber
- hackernews
---
## Outils de jeu piratés diffusent un RAT Java

Des acteurs malveillants exploitent des plateformes de navigation et de messagerie pour distribuer un cheval de Troie d'accès à distance (RAT) en utilisant des utilitaires de jeu compromis. Ces outils, une fois exécutés, installent un RAT Java polyvalent capable d'agir comme chargeur, exécuteur, téléchargeur et RAT. La chaîne d'attaque vise à passer inaperçue en supprimant le téléchargeur initial et en configurant des exclusions dans Microsoft Defender pour les composants du RAT. La persistance est assurée par des tâches planifiées et des scripts de démarrage. Le RAT communique avec un serveur de commande et contrôle (C2) pour exfiltrer des données et déployer des charges utiles supplémentaires.

### Points Clés
*   Distribution d'un RAT Java via des utilitaires de jeu piratés.
*   Utilisation de plateformes de navigation et de messagerie pour la distribution.
*   Mécanismes d'évasion de détection, y compris la suppression des fichiers initiaux et la configuration d'exclusions antivirus.
*   Mise en place de persistance via des tâches planifiées et des scripts de démarrage.
*   Fonctionnalités multiples du RAT : chargeur, exécuteur, téléchargeur et RAT.
*   Communication avec un serveur C2 pour la commande et le contrôle, l'exfiltration de données et le déploiement de charges utiles.

### Vulnérabilités
Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article concernant la technique d'infection elle-même, mais le RAT exploite l'exécution de code arbitraire et potentiellement des vulnérabilités systèmes pour le déploiement et la persistance.

### Recommandations
*   Auditer les exclusions configurées dans Microsoft Defender.
*   Vérifier et supprimer les tâches planifiées et scripts de démarrage potentiellement malveillants.
*   Isoler les terminaux affectés par l'infection.
*   Réinitialiser les identifiants des utilisateurs actifs sur les systèmes compromis.

---
[Source](https://thehackernews.com/2026/02/trojanized-gaming-tools-spread-java.html){:target="_blank"}
