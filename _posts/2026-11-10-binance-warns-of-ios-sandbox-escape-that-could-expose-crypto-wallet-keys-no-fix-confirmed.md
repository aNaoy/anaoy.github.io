---
title: 'Binance Warns of iOS Sandbox Escape That Could Expose Crypto Wallet Keys, No Fix Confirmed'
date: 2026-11-10
permalink: /posts/2026/11/10/binance-warns-of-ios-sandbox-escape-that-could-expose-crypto-wallet-keys-no-fix-confirmed/
tags:
- veille-cyber
- hackernews
---
### Risque d'évasion de bac à sable (sandbox) sur iOS : menace pour les portefeuilles crypto

Une faille d'évasion de bac à sable nommée **"worse_query"** permet à une application malveillante d'accéder aux fichiers privés d'autres applications sur iOS 26 et 27. Cette vulnérabilité expose des données sensibles, telles que les clés privées, les phrases de récupération (seed phrases) et les identifiants de connexion.

**Points clés :**
* **Mécanisme :** La faille exploite la configuration des conteneurs "App Group". Elle ne nécessite ni jailbreak ni exploitation du noyau pour lire, modifier ou supprimer les données d'autres applications.
* **Diffusion :** Le code est disponible sur GitHub. Des applications tierces (comme "WQ Files"), installables via le sideloading (AltStore, SideStore), utilisent cette faille.
* **Réaction d'Apple :** Les récentes mises à jour (iOS 27.2.1 et 26.7.3) ne corrigent pas explicitement cette vulnérabilité, et aucun correctif officiel n'a été confirmé à ce jour.
* **État de la menace :** Aucune attaque active ou vol de fonds n'a été rapporté pour le moment, bien que la surface d'attaque soit réelle.

**Vulnérabilités :**
* **CVE :** Aucune CVE n'a encore été attribuée à cette vulnérabilité.

**Recommandations :**
* **Suppression :** Désinstaller immédiatement toute application installée via des sources non fiables ou des outils de sideloading.
* **Mise à jour :** Maintenir iOS et toutes les applications à jour, bien que la faille persiste pour l'instant.
* **Sécurisation :** En cas de suspicion de compromission, transférer les fonds vers un nouveau portefeuille généré sur un appareil propre et réinitialiser toutes les sessions de connexion actives.

---
[Source](https://thehackernews.com/2026/11/binance-warns-of-ios-sandbox-escape.html){:target="_blank"}
