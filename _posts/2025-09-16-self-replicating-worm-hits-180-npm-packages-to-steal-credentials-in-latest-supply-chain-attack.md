---
title: 'Self-Replicating Worm Hits 180+ npm Packages to Steal Credentials in Latest Supply Chain Attack'
date: 2025-09-16
permalink: /posts/2025/09/16/self-replicating-worm-hits-180-npm-packages-to-steal-credentials-in-latest-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Attaque Virale Auto-Réplicante sur npm

Un ver informatique auto-réplicant a compromis plus de 180 paquets du registre npm, visant à dérober des identifiants de développeurs. Cette attaque, baptisée "Shai-Hulud", infecte automatiquement les paquets en aval, créant une chaîne de compromission.

**Fonctionnement de l'attaque :**

Les versions infectées des paquets téléchargent une archive, modifient le fichier `package.json`, injectent un script local (`bundle.js`), puis reconditionnent et republient le paquet. Ce script utilise l'outil TruffleHog pour scanner les machines des développeurs à la recherche de secrets (tokens et identifiants cloud comme GITHUB_TOKEN, NPM_TOKEN, AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY). Il tente de valider les tokens npm via l'endpoint "whoami", interagit avec les API GitHub et cherche des identifiants éphémères dans les agents de build cloud. Les identifiants compromis, notamment les tokens d'accès personnels GitHub, sont utilisés pour créer un workflow GitHub Actions dans `.github/workflows` afin d'exfiltrer les données vers un serveur contrôlé par l'attaquant. De plus, le ver tente de créer des copies publiques de tous les dépôts privés des utilisateurs compromis.

**Paquets Concernés (liste non exhaustive) :**

*   `angulartics2@14.1.2`
*   `@ctrl/tinycolor@4.1.1, @4.1.2`
*   `@nativescript-community/ui-image@4.5.6`
*   `ngx-color@10.0.2`
*   `@crowdstrike/commitlint@8.1.1, 8.1.2`
*   `@crowdstrike/logscale-dashboard@1.205.2`
*   `eslint-config-crowdstrike@11.0.3`
*   `rxnt-authentication@0.0.6` (considéré comme Patient Zéro)

**Vulnérabilités :**

Aucune CVE spécifique n'est mentionnée pour cette attaque, car elle exploite une combinaison de compromission de comptes développeurs, d'injection de code malveillant dans des paquets légitimes et de l'utilisation d'outils de sécurité légitimes pour le vol de données. L'aspect auto-réplicant est une caractéristique évoluée de cette menace.

**Recommandations :**

*   Auditer les environnements pour détecter la présence des paquets compromis.
*   Révocquer et régénérer les tokens npm et autres secrets exposés.
*   Mettre à jour les paquets affectés vers des versions non compromises.
*   Surveiller l'activité suspecte et les créations de dépôts inattendues.
*   Sécuriser les comptes de développeurs et les accès aux registres de paquets.

Il est important de noter qu'une campagne de phishing distincte ciblant les utilisateurs de `crates.io` (registre Rust) a également été signalée, cherchant à voler des identifiants GitHub via une fausse page de connexion.

---
[Source](https://thehackernews.com/2025/09/40-npm-packages-compromised-in-supply.html){:target="_blank"}
