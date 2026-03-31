---
title: 'Hacker charged with stealing $53 million from Uranium crypto exchange'
date: 2026-03-31
permalink: /posts/2026/03/31/hacker-charged-with-stealing-53-million-from-uranium-crypto-exchange/
tags:
- veille-cyber
- bleepingcomp
---
### Inculpation pour le piratage à 53 millions de dollars de la plateforme Uranium Finance

Jonathan Spalletta, un résident du Maryland, a été inculpé pour le piratage de la plateforme d'échange décentralisée Uranium Finance en avril 2021, ayant entraîné le vol de 53,3 millions de dollars et la fermeture définitive de l'entreprise. L'auteur a utilisé des techniques de blanchiment via le mélangeur Tornado Cash pour masquer ses gains, avant d'être identifié par des enquêteurs indépendants et arrêté par les autorités fédérales.

**Points clés :**
*   **Mode opératoire :** L'attaquant a exploité à deux reprises des vulnérabilités critiques dans les contrats intelligents (smart contracts) de la plateforme.
*   **Blanchiment :** Les fonds volés ont été transférés via Tornado Cash, puis convertis en actifs de collection de grande valeur (cartes Magic, Pokémon, pièces antiques) et en cryptomonnaies.
*   **Récupération :** Les autorités ont saisi pour environ 31 millions de dollars d'actifs et de nombreux objets de collection au domicile du suspect.

**Vulnérabilités exploitées :**
*   **Manipulation de variables :** Exploitation de la variable `AmountWithBonus` permettant des retraits sans dépôt de jetons.
*   **Erreur de logique de vérification :** Utilisation d'une erreur de saisie dans le code de vérification des transactions (valeur de 1 000 au lieu de 10 000), permettant de drainer 90 % des liquidités des pools de la plateforme.

**Recommandations :**
*   **Audit rigoureux des Smart Contracts :** Soumettre systématiquement le code aux audits de sécurité par des tiers indépendants avant tout déploiement sur la blockchain.
*   **Validation stricte des entrées :** Implémenter des mécanismes de vérification robustes dans la logique des contrats intelligents pour empêcher la manipulation des variables de retrait.
*   **Gestion des primes aux bugs :** Mettre en place des programmes de "Bug Bounty" officiels et transparents pour éviter que des failles ne soient exploitées sous forme d'extorsion.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-charged-with-stealing-53-million-from-uranium-crypto-exchange/){:target="_blank"}
