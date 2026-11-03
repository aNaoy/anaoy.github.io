---
title: 'Chainstack Reports Production Systems Breach Exposing Customer Data and Password Hashes'
date: 2026-11-03
permalink: /posts/2026/11/03/chainstack-reports-production-systems-breach-exposing-customer-data-and-password-hashes/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque par IA contre Chainstack : Données clients exposées

Chainstack, fournisseur d'infrastructures blockchain, a subi une intrusion dans son environnement de production entre le 26 et le 31 octobre 2026. L'attaquant a exploité une vulnérabilité via un composant tiers pour infiltrer le système. Cet incident s'inscrit dans une campagne plus large utilisant des agents autonomes basés sur l'IA (nommée ARTEX), ciblant plusieurs entreprises technologiques, dont WorkOS et Chainalysis.

**Points clés :**
* **Données compromises :** Noms d'organisations, noms des détenteurs de comptes, adresses e-mail et empreintes de mots de passe (hashs).
* **Risques supplémentaires :** Accès potentiel aux identifiants de nœuds, bien qu'aucune preuve d'exfiltration n'ait été confirmée.
* **Tendance :** Utilisation croissante d'agents IA pour automatiser les stratégies d'attaque, augmenter la vitesse d'exécution et exploiter les faiblesses applicatives.

**Vulnérabilités mentionnées :**
* Bien que l'intrusion chez Chainstack repose sur un composant tiers non spécifié, des attaques similaires (ex: DIVD) ont exploité des failles zero-day dans le système de gestion de tickets Zammad : **CVE-2026-102489** et **CVE-2026-102490**.

**Recommandations :**
* **Réinitialisation immédiate :** Changer les mots de passe (particulièrement si réutilisés sur d'autres services) et faire pivoter les identifiants de nœuds.
* **Sécurité des accès :** Régénérer les clés API de la plateforme Chainstack.
* **Vigilance accrue :** Surveiller les communications entrantes pour détecter d'éventuelles tentatives de phishing ciblées, facilitées par les données exfiltrées.

---
[Source](https://thehackernews.com/2026/11/chainstack-reports-production-systems.html){:target="_blank"}
