---
title: 'OptinMonster WordPress plugin hacked in CDN supply-chain attack'
date: 2026-06-15
permalink: /posts/2026/06/15/optinmonster-wordpress-plugin-hacked-in-cdn-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement sur les extensions WordPress d'Awesome Motive

Les extensions WordPress **OptinMonster**, **TrustPulse** et **PushEngage** ont été compromises via une attaque par chaîne d'approvisionnement ciblant le réseau de distribution de contenu (CDN) de l'éditeur Awesome Motive. Les attaquants ont injecté du code JavaScript malveillant, permettant une prise de contrôle totale des sites infectés.

**Points clés :**
*   **Vecteur d'entrée :** Exploitation d'une vulnérabilité dans le plugin *UpdraftPlus* sur un serveur marketing secondaire, permettant le vol des clés API du CDN.
*   **Mode opératoire :** Le script malveillant s'exécutait uniquement lors de la connexion d'un administrateur WordPress. Il volait les jetons d'authentification pour créer un compte administrateur pirate, installer des backdoors (ex: "Content Delivery Helper", "Database Optimizer") et déployer un shell web.
*   **Impact :** Accès distant complet, exécution de code PHP arbitraire et exfiltration de données via un domaine usurpant *Tidio*.

**Vulnérabilité :**
*   Exploitation d'une faille connue dans le plugin **UpdraftPlus** (permettant l'accès initial au serveur).

**Recommandations pour les administrateurs de sites impactés :**
*   **Supprimer** les comptes administrateurs suspects (ex: `developer_api1`, `dev_xxxxxx`).
*   **Rechercher et supprimer** les extensions "backdoor" dissimulées dans le répertoire `wp-content/plugins`.
*   **Effectuer** un scan antivirus complet côté serveur.
*   **Réinitialiser** les mots de passe administrateur, les clés API, les identifiants de base de données et les clés de sécurité (*salts*) WordPress.

---
[Source](https://www.bleepingcomputer.com/news/security/optinmonster-wordpress-plugin-hacked-in-cdn-supply-chain-attack/){:target="_blank"}
