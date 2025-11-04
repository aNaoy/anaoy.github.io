---
title: 'Hacker steals over $120 million from Balancer DeFi crypto protocol'
date: 2025-11-04
permalink: /posts/2025/11/04/hacker-steals-over-120-million-from-balancer-defi-crypto-protocol/
tags:
- veille-cyber
- bleepingcomp
---
### Le Protocole BalancerVictime d'une Fraude Massive

Le protocole Balancer, un écosystème de finance décentralisée (DeFi) basé sur la blockchain Ethereum, a subi un piratage majeur touchant ses pools V2, entraînant des pertes estimées à plus de 128 millions de dollars. L'incident a affecté spécifiquement les "Compostable Stable Pools".

**Points Clés :**
*   Le piratage a eu lieu le 3 novembre 2025, vers 7h48 UTC.
*   Seuls les pools V2 "Compostable Stable Pools" sont concernés ; les pools V3 ne sont pas impactés.
*   Balancer a mis en garde les utilisateurs contre d'éventuelles tentatives d'hameçonnage suite à cet incident.
*   Une tentative de fraude a été observée, où un individu s'est fait passer pour Balancer afin de proposer une "prime de chevalier blanc" au pirate en échange de la restitution des fonds.

**Vulnérabilités Potentielles :**
*   **Erreur d'arrondi de précision dans les calculs de swap :** Une petite divergence lors de l'arrondi des montants des jetons dans les opérations de swap a pu être exploitée de manière répétée, capitalisant sur les pertes cumulées pour créer une distorsion des prix.
*   **Gestion inappropriée des autorisations et des rappels (callbacks) :** Il est également suggéré qu'un contrat malveillant aurait pu manipuler les appels aux vaults lors de l'initialisation des pools, contournant les protections et permettant des manipulations non autorisées des soldes et des swaps entre pools interconnectés.

**Recommandations :**
*   Balancer travaille avec des chercheurs en sécurité pour analyser l'incident et promet de fournir une analyse post-mortem détaillée.
*   Il est crucial que les utilisateurs restent vigilants face aux arnaques et aux tentatives d'hameçonnage qui pourraient exploiter cette situation.
*   Bien que non confirmé, le contexte actuel de piratages massifs de cryptomonnaies, souvent attribués à des acteurs nord-coréens, pourrait être pertinent.

---
[Source](https://www.bleepingcomputer.com/news/cryptocurrency/hacker-steals-over-120-million-from-balancer-defi-crypto-protocol/){:target="_blank"}
