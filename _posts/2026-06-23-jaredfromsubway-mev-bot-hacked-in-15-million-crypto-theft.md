---
title: 'JaredFromSubway MEV bot hacked in $15 million crypto theft'
date: 2026-06-23
permalink: /posts/2026/06/23/jaredfromsubway-mev-bot-hacked-in-15-million-crypto-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Vol de 15 millions de dollars par manipulation de bot MEV

Le célèbre bot de "sandwich attack" sur Ethereum, *JaredFromSubway*, a subi une perte de 15 millions de dollars suite à une attaque sophistiquée exploitant sa logique de détection d'opportunités de trading.

**Points clés :**
*   **Mode opératoire :** L'attaquant a déployé de faux contrats lucratifs pour inciter le bot à interagir avec eux.
*   **Méthode :** Le bot, en analysant ces opportunités frauduleuses, a automatiquement accordé des autorisations de dépenses (approvals) à des contrats contrôlés par l'attaquant.
*   **Exécution différée :** Après avoir accumulé des permissions valides sur une longue période, l'attaquant a utilisé la fonction `transferFrom` pour drainer les fonds (WETH, USDC, USDT).
*   **Réaction :** Le propriétaire du bot a tenté de négocier la récupération des fonds via des primes allant jusqu'à 7,5 millions de dollars, sans succès immédiat.

**Vulnérabilités :**
*   **Logique de validation :** Absence de vérification rigoureuse de la légitimité des contrats tiers lors de l'octroi automatique d'approbations ERC-20.
*   **Gestion des permissions :** Le système ne révoquait pas systématiquement les autorisations après l'échec ou la finalisation d'une transaction, permettant l'accumulation de droits de retrait sur le portefeuille.
*   *Note : Aucune CVE spécifique n'a été attribuée, car il s'agit d'une vulnérabilité liée à la logique applicative du bot et non à une faille du protocole Ethereum.*

**Recommandations :**
*   **Validation stricte des contrats :** Implémenter des listes blanches ou des mécanismes de vérification de réputation pour tout contrat avec lequel le bot interagit.
*   **Gestion sécurisée des approbations :** Adopter des patterns d'approbation à usage unique ou limiter strictement le montant et la durée des permissions accordées.
*   **Audit de logique métier :** Soumettre les algorithmes de décision des bots de trading à des audits de sécurité pour détecter les vecteurs d'attaque par manipulation de données de marché.

---
[Source](https://www.bleepingcomputer.com/news/security/jaredfromsubway-mev-bot-hacked-in-15-million-crypto-theft/){:target="_blank"}
