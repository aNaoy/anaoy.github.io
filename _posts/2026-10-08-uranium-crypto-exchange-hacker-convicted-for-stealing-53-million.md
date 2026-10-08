---
title: 'Uranium crypto exchange hacker convicted for stealing $53 million'
date: 2026-10-08
permalink: /posts/2026/10/08/uranium-crypto-exchange-hacker-convicted-for-stealing-53-million/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation pour le piratage de 53 millions de dollars de la plateforme Uranium Finance

Jonathan Spalletta, un habitant du Maryland, a été reconnu coupable du piratage de la plateforme d'échange décentralisée Uranium Finance en avril 2021, entraînant la fermeture définitive du service.

**Points clés :**
* **Détournement de fonds :** L'attaquant a dérobé environ 53,3 millions de dollars en cryptomonnaies via deux attaques distinctes.
* **Blanchiment :** Les fonds ont été blanchis via le mixeur Tornado Cash et diverses plateformes décentralisées, puis convertis en objets de collection de luxe (cartes Magic, Pokémon, pièces antiques).
* **Récupération :** Les autorités ont saisi les objets acquis et récupéré environ 31 millions de dollars en cryptomonnaies dans les portefeuilles liés au pirate.
* **Sanctions encourues :** Spalletta risque jusqu'à 30 ans de prison cumulés pour fraude informatique et blanchiment d'argent.

**Vulnérabilités exploitées :**
L'attaquant a exploité des erreurs critiques dans le code des contrats intelligents (Smart Contracts) de la plateforme :
* **Première attaque :** Utilisation de commandes de retrait pour des jetons nuls (zero-token), forçant le versement de récompenses indues.
* **Seconde attaque :** Erreur de logique dans la vérification des transactions (valeur mal calibrée), permettant de retirer 90 % de la liquidité tout en déposant un montant nul.

**Recommandations de sécurité :**
* **Audit rigoureux du code :** Soumettre systématiquement les contrats intelligents à des audits de sécurité professionnels avant tout déploiement.
* **Gestion des limites de transaction :** Implémenter des contrôles stricts sur les paramètres d'entrée pour éviter les manipulations de logique arithmétique.
* **Monitoring en temps réel :** Mettre en place des mécanismes de détection d'anomalies sur les pools de liquidité pour identifier et bloquer immédiatement les comportements de retrait suspects.
* **Gestion des privilèges :** Éviter les mécanismes qui permettent de drainer des fonds via des commandes de retrait non validées ou des systèmes de "bug bounty" extorqués sous la contrainte.

---
[Source](https://www.bleepingcomputer.com/news/security/uranium-crypto-exchange-hacker-found-guilty-of-53-million-theft/){:target="_blank"}
