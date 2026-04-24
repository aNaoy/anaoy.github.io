---
title: '26 FakeWallet Apps Found on Apple App Store Targeting Crypto Seed Phrases'
date: 2026-04-24
permalink: /posts/2026/04/24/26-fakewallet-apps-found-on-apple-app-store-targeting-crypto-seed-phrases/
tags:
- veille-cyber
- hackernews
---
### Campagne « FakeWallet » : Des applications malveillantes sur l'App Store

Des chercheurs en cybersécurité ont identifié 26 applications frauduleuses sur l'App Store d'Apple usurpant l'identité de portefeuilles de cryptomonnaies populaires (MetaMask, Ledger, Coinbase, etc.). Ces applications, principalement diffusées auprès des utilisateurs basés en Chine, visent à dérober les phrases de récupération (seed phrases) et les clés privées des victimes pour vider leurs actifs numériques.

#### Points clés
*   **Mode opératoire :** Utilisation d'applications « miroir » avec des noms légèrement modifiés ou des icônes trompeuses. Certaines applications servent de passerelles pour installer des logiciels malveillants via des profils de configuration d'entreprise (Enterprise Provisioning Profiles).
*   **Techniques de vol :** Injection de code malveillant dans des portefeuilles légitimes, utilisation de pages de phishing pour simuler une « vérification » de compte, ou recours à la reconnaissance optique de caractères (OCR) pour capturer les phrases mnémoniques affichées à l'écran.
*   **Lien potentiel :** La campagne est suspectée d'être liée aux acteurs derrière le cheval de Troie « SparkKitty ».
*   **Menace complémentaire :** Parallèlement, le framework Android « MiningDropper » (ou BeatBanker) a été identifié, utilisant des applications usurpant des services bancaires pour déployer des mineurs de cryptomonnaies et des chevaux de Troie d'accès distant.

#### Vulnérabilités
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'**ingénierie sociale** et le **détournement de processus de distribution légitimes** (App Store et profils d'approvisionnement d'entreprise iOS).

#### Recommandations
*   **Téléchargement sécurisé :** Ne télécharger des portefeuilles de cryptomonnaies que depuis le site officiel du développeur ou les liens officiels vérifiés.
*   **Vigilance sur les autorisations :** Se méfier des applications demandant l'installation de profils de configuration tiers ou des autorisations excessives (OCR, accès écran).
*   **Hygiène numérique :** Ne jamais saisir de phrase de récupération (seed phrase) sur une page web ou dans une application tierce, sauf lors de la configuration initiale sur une interface de confiance.
*   **Vérification :** Croiser systématiquement le nom de l'éditeur et les avis avant d'installer une application financière.

---
[Source](https://thehackernews.com/2026/04/26-fakewallet-apps-found-on-apple-app.html){:target="_blank"}
