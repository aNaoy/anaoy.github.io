---
title: 'Liquid Hackers Return 3,400 Bitcoin Taken via Elements Bug, Still Holding $47M in BTC'
date: 2026-09-08
permalink: /posts/2026/09/08/liquid-hackers-return-3400-bitcoin-taken-via-elements-bug-still-holding-47m-in-btc/
tags:
- veille-cyber
- hackernews
---
### Incident de sécurité sur le réseau Liquid : piratage et récupération partielle de fonds

Le réseau Liquid, une sidechain Bitcoin, a subi un piratage exploitant une vulnérabilité logicielle permettant le retrait non autorisé d'environ 4 000 BTC. Suite à des échanges sur la blockchain, les attaquants — se présentant comme des « white hats » — ont restitué 3 400 BTC, conservant toutefois 598,5 BTC (environ 47 millions de dollars). Le réseau a été temporairement mis en pause par Blockstream pour sécuriser la plateforme.

**Points clés :**
* **Nature de l'attaque :** Exploitation d'un bug dans le logiciel *Elements* utilisé par le réseau Liquid.
* **Volume détourné :** Environ 4 000 BTC (soit 95 % des réserves totales de la sidechain).
* **Statut actuel :** Le réseau est à l'arrêt, les passerelles (bridge nodes) ont été mises à jour, et une reprise coordonnée est en cours de préparation.
* **Controverse :** La conservation de près de 600 BTC par les attaquants suscite des doutes sur leur réelle intention éthique, certains experts y voyant une manœuvre d'extorsion plutôt qu'une démarche de « white hat ».

**Vulnérabilités :**
* Le problème provient d'un bug spécifique au sein du logiciel **Elements** ayant permis de générer du L-BTC (le jeton adossé au Bitcoin) de manière illégitime pour déclencher un « peg-out ». Aucune clé privée n'a été compromise. (Aucune CVE spécifique n'a été publiée à ce jour).

**Recommandations :**
* **Pour les utilisateurs :** Ne pas effectuer de transactions vers les adresses de « peg-in » (dépôt) de Liquid tant que la reprise du réseau n'a pas été officiellement confirmée par Blockstream.
* **Pour les opérateurs :** S'assurer que tous les nœuds du réseau ont été mis à jour avec le correctif déployé par Blockstream.
* **Sécurité globale :** Renforcer les audits de sécurité sur les composants critiques de la blockchain *Elements* afin de prévenir la création arbitraire de jetons adossés.

---
[Source](https://thehackernews.com/2026/09/liquid-hackers-return-3400-bitcoin.html){:target="_blank"}
