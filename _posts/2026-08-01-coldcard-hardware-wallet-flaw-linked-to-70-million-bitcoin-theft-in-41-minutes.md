---
title: 'Coldcard Hardware Wallet Flaw Linked to $70 Million Bitcoin Theft in 41 Minutes'
date: 2026-08-01
permalink: /posts/2026/08/01/coldcard-hardware-wallet-flaw-linked-to-70-million-bitcoin-theft-in-41-minutes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique des portefeuilles Coldcard : 70 millions de dollars dérobés

Une faille dans le micrologiciel des portefeuilles matériels **Coldcard** a permis le vol de 1 082,65 BTC (environ 70 millions de dollars). L'attaque exploite une erreur d'intégration présente depuis mars 2021 qui a compromis la génération des clés privées.

**Points clés :**
* **Cause racine :** Une erreur de configuration dans le micrologiciel a forcé le système à utiliser un générateur de nombres pseudo-aléatoires (PRNG) logiciel prévisible, au lieu du générateur matériel (RNG) sécurisé du processeur STM32.
* **Mécanisme d'attaque :** La faiblesse repose sur le fait que la graine (seed) est générée à partir de données prévisibles (ID unique de la puce, état du minuteur). Un attaquant peut ainsi reproduire hors ligne les séquences de clés privées potentielles et vérifier leur correspondance avec des adresses Bitcoin actives sur la blockchain.
* **Portée :** La vulnérabilité dépend de la version du micrologiciel utilisée au moment de la création du portefeuille. Les modèles Mk2, Mk3, Mk4, Mk5 et Q sont concernés sur plusieurs versions antérieures aux correctifs publiés le 31 juillet.

**Vulnérabilité :**
* Faiblesse cryptographique liée à une entropie insuffisante lors de la génération de la graine (Seed) due à une mauvaise implémentation du `MicroPython Yasmarang PRNG` (pas de CVE spécifique attribué publiquement à ce jour, mais documentée comme une erreur de configuration de build).

**Recommandations :**
* **Migrer immédiatement :** L'installation du micrologiciel correctif ne répare pas une graine déjà compromise. Les utilisateurs doivent générer une toute nouvelle graine sur un appareil mis à jour et transférer leurs fonds vers cette nouvelle adresse.
* **Vérification de l'entropie :** Coinkite précise qu'une graine générée en utilisant manuellement au moins 50 lancers de dés (méthode de génération manuelle) n'est pas affectée par ce bug.
* **Sécurité supplémentaire :** Bien qu'une phrase secrète (passphrase) BIP-39 robuste puisse offrir une protection supplémentaire, il est fortement recommandé de remplacer totalement la graine par mesure de précaution.

---
[Source](https://thehackernews.com/2026/08/coldcard-hardware-wallet-flaw-linked-to.html){:target="_blank"}
