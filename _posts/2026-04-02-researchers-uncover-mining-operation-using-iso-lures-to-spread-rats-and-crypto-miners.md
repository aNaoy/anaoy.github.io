---
title: 'Researchers Uncover Mining Operation Using ISO Lures to Spread RATs and Crypto Miners'
date: 2026-04-02
permalink: /posts/2026/04/02/researchers-uncover-mining-operation-using-iso-lures-to-spread-rats-and-crypto-miners/
tags:
- veille-cyber
- hackernews
---
### Campagne REF1695 : Propagation de malwares via des installeurs frauduleux

L'opération REF1695, active depuis novembre 2023, déploie des chevaux de Troie d'accès à distance (RAT) et des mineurs de cryptomonnaies en utilisant des fichiers ISO comme vecteur d'infection. Les attaquants exploitent l'ingénierie sociale pour contourner les protections natives de Windows et monétisent leurs activités par le minage de Monero (XMR) ainsi que par la fraude publicitaire (CPA).

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de fichiers ISO contenant des installeurs piégés et des instructions pour contourner manuellement "Microsoft Defender SmartScreen".
*   **Implant CNB Bot :** Un nouveau malware .NET qui télécharge des charges utiles, se met à jour et communique avec un serveur de commande (C2) via HTTP.
*   **Techniques de persistance :** Utilisation de tâches planifiées et d'un processus "watchdog" pour restaurer les composants malveillants en cas de suppression.
*   **Abus de services légitimes :** Exploitation de GitHub pour héberger des binaires malveillants afin de contourner les détections basées sur la réputation des domaines.
*   **Gain financier :** La campagne a généré environ 9 400 USD en Monero, confirmant sa rentabilité.

**Vulnérabilités exploitées :**
*   **WinRing0x64.sys :** Bien qu'il s'agisse d'un pilote légitime, il est utilisé pour obtenir un accès au niveau du noyau (kernel) afin de modifier les paramètres CPU et maximiser le taux de hachage du minage. (Note : ce type d'abus de pilotes signés mais vulnérables est un vecteur classique de *Bring Your Own Vulnerable Driver* - BYOVD).

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à ne jamais suivre les instructions visant à contourner manuellement les avertissements de sécurité ("More info" / "Run anyway").
*   **Configuration de sécurité :** Restreindre les autorisations d'exécution des fichiers ISO et surveiller les modifications des exclusions de Microsoft Defender.
*   **Filtrage réseau :** Bloquer ou surveiller les communications sortantes vers des services de stockage tiers (comme GitHub) lorsqu'elles sont initiées par des processus système ou des installeurs non autorisés.
*   **Gestion des privilèges :** Limiter les droits d'administration locale pour empêcher l'installation de pilotes malveillants ou le chargement de composants au niveau noyau.

---
[Source](https://thehackernews.com/2026/04/researchers-uncover-mining-operation.html){:target="_blank"}
