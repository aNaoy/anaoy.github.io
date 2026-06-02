---
title: 'Hackers hijack thousands of sites for ClickFix and FakeUpdate attacks'
date: 2026-06-02
permalink: /posts/2026/06/02/hackers-hijack-thousands-of-sites-for-clickfix-and-fakeupdate-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne DriveSurge : Multiplication des attaques via ClickFix et FakeUpdates

Le groupe cybercriminel « DriveSurge » orchestre une campagne de distribution de malwares à grande échelle en compromettant des milliers de sites web légitimes. Le groupe agit comme un courtier en accès initial, utilisant un système de distribution de trafic (TDS) nommé zTDS pour rediriger les internautes vers des infrastructures malveillantes en fonction de leur profil.

**Points clés :**
*   **Techniques d'ingénierie sociale :** Utilisation de tactiques « ClickFix » (invitant l'utilisateur à exécuter des commandes PowerShell pour résoudre des erreurs fictives) et « FakeUpdates » (fausses mises à jour de navigateurs populaires comme Chrome, Firefox, Edge, etc.).
*   **Portée multiplateforme :** Bien que centrée sur Windows, la campagne cible également macOS via des payloads JavaScript obfusqués qui détournent le presse-papier.
*   **Mode opératoire :** Injection de scripts malveillants (`t.js?site=<id>`) sur des sites compromis pour rediriger les victimes à leur insu.
*   **Modèle économique :** Fonctionnement basé sur le « pay-per-install » (paiement à l'installation).

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exploitation de la crédulité des utilisateurs et sur l'injection de scripts dans des sites web vulnérables, plutôt que sur une faille logicielle unique.

**Recommandations :**
*   **Mises à jour sécurisées :** Effectuez uniquement les mises à jour de navigateurs via les menus internes de l'application (paramètres > à propos).
*   **Prudence face aux commandes :** Ne jamais copier-coller ou exécuter des commandes provenant de sites web dans un terminal ou une invite de commande (PowerShell/CMD).
*   **Vigilance :** Se méfier des messages d'erreur intrusifs demandant une intervention technique immédiate sur le navigateur.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hijack-thousands-of-sites-for-clickfix-and-fakeupdate-attacks/){:target="_blank"}
