---
title: 'FakeWallet crypto stealer spreading through iOS apps in the App Store'
date: 2026-04-20
permalink: /posts/2026/04/20/fakewallet-crypto-stealer-spreading-through-ios-apps-in-the-app-store/
tags:
- veille-cyber
- securelist
---
### Campagne de vol de cryptomonnaies via des applications iOS piégées

Une campagne malveillante, active depuis fin 2025, utilise des applications de type « porte-monnaie crypto » contrefaites (typosquatting) pour infecter des appareils iOS et dérober des phrases de récupération et des clés privées. Bien que principalement détectée sur l'App Store chinois, cette menace, baptisée **FakeWallet**, cible les utilisateurs globalement.

**Points clés :**
* **Propagation :** Les applications, déguisées en portefeuilles populaires (MetaMask, Ledger, Trust Wallet, Coinbase, etc.), dirigent les utilisateurs vers des pages web tierces pour installer des versions « trojanisées » via des profils de provisionnement d'entreprise.
* **Technique d'injection :** Les attaquants utilisent l'injection de bibliothèques dynamiques (`.dylib`) ou modifient directement le code source (notamment pour React Native) pour intercepter les saisies utilisateur.
* **Extraction :** Les données sensibles sont chiffrées en RSA et encodées en Base64 avant d'être exfiltrées vers des serveurs de commande et contrôle (C2).
* **Ciblage :** Les portefeuilles « à chaud » sont directement interceptés, tandis que les portefeuilles « à froid » (type Ledger) font l'objet d'attaques par hameçonnage via de fausses interfaces de vérification intégrées.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, la campagne exploitant des **mécanismes légitimes d'iOS** (profils de provisionnement d'entreprise et sideloading) pour contourner la sécurité de l'App Store.

**Recommandations :**
* **Vérification :** Téléchargez uniquement les applications de portefeuilles depuis les sites officiels des fournisseurs et vérifiez la cohérence du développeur.
* **Prudence avec les profils :** N'installez jamais de profils de provisionnement d'entreprise provenant de sources non fiables.
* **Scepticisme :** Méfiez-vous des applications demandant une « vérification de sécurité » ou la saisie d'une phrase de récupération (seed phrase) en dehors des flux officiels de configuration initiale.
* **Détection :** Les solutions de sécurité (comme Kaspersky) détectent ces menaces sous les identifiants `HEUR:Trojan-PSW.IphoneOS.FakeWallet.*` et `HEUR:Trojan.IphoneOS.FakeWallet.*`.

---
[Source](https://securelist.com/fakewallet-cryptostealer-ios-app-store/119474/){:target="_blank"}
