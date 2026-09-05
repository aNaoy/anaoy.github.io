---
title: 'Over 5,400 hacked sites serve ClickFix payloads stored on the blockchain'
date: 2026-09-05
permalink: /posts/2026/09/05/over-5400-hacked-sites-serve-clickfix-payloads-stored-on-the-blockchain/
tags:
- veille-cyber
- bleepingcomp
---
### Propagation de malwares via la blockchain : La menace "EtherHiding"

Une vaste campagne cybercriminelle utilise plus de 5 400 sites web compromis (principalement WordPress et PrestaShop) pour diffuser des charges malveillantes hébergées sur le réseau BNB Smart Chain (BSC) Testnet. Cette technique, appelée « EtherHiding », exploite la résilience des contrats intelligents pour stocker et mettre à jour dynamiquement des scripts malveillants, rendant leur suppression extrêmement difficile.

**Points clés :**
* **Méthodologie :** Les sites infectés injectent un script qui récupère la charge utile directement depuis la blockchain.
* **Vecteur d'attaque initial :** Une technique de « ClickFix » incite les utilisateurs à exécuter une commande PowerShell via une fausse fenêtre CAPTCHA.
* **Évolution technique :** Les attaquants ont récemment intégré un « stager » WebRTC capable d'établir un canal de communication chiffré et furtif. Le code malveillant est exécuté directement dans la mémoire du navigateur sans jamais être écrit sur le disque.
* **Volume d'activité :** Plus de 300 nouveaux sites sont infectés quotidiennement, avec des pics d'activité dépassant 500 appels aux terminaux RPC du BSC Testnet par jour.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car l'attaque repose sur une exploitation légitime des fonctionnalités de smart contracts et une ingénierie sociale visant l'utilisateur final.

**Recommandations :**
* **Blocage réseau :** Restreindre l'accès à l'ensemble des terminaux RPC du BSC Testnet (liste des IOC disponible via les travaux de Netskope Threat Labs).
* **Surveillance :** Surveiller étroitement le trafic UDP non lié au web afin de détecter les connexions WebRTC suspectes.
* **Sensibilisation :** Éduquer les utilisateurs sur les dangers liés à l'exécution de commandes PowerShell provenant d'invites de sécurité suspectes (fausses alertes CAPTCHA).

---
[Source](https://www.bleepingcomputer.com/news/security/over-5-400-hacked-sites-serve-clickfix-payloads-stored-on-the-blockchain/){:target="_blank"}
