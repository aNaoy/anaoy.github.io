---
title: 'COLDCARD wallet RNG flaw likely linked to $88 million Bitcoin theft'
date: 2026-08-03
permalink: /posts/2026/08/03/coldcard-wallet-rng-flaw-likely-linked-to-88-million-bitcoin-theft/
tags:
- veille-cyber
- bleepingcomp
---
# Vol de 88 millions de dollars en Bitcoin via une faille RNG sur COLDCARD

Une vulnérabilité critique dans le micrologiciel (firmware) des portefeuilles matériels COLDCARD a permis le vol d'environ 1 367 Bitcoin (soit 88,6 millions de dollars) sur plus de 4 500 adresses. Les attaquants ont exploité une faille dans la génération des nombres aléatoires (RNG) pour reconstituer les clés privées des victimes.

### Points clés
*   **Mécanisme d'attaque :** Une erreur d'intégration force le RNG à utiliser un générateur déterministe prévisible (MicroPython/Yasmarang) au lieu du générateur matériel sécurisé (STM32). 
*   **Exploitation :** Les attaquants ont pu générer hors ligne des graines de portefeuille probables, identifier les adresses correspondantes sur la blockchain, puis automatiser le transfert des fonds.
*   **Ciblage :** Les transactions, hautement automatisées et très coûteuses en frais, suggèrent que les attaquants avaient préalablement identifié et étudié les portefeuilles vulnérables.
*   **Périmètre :** Les modèles affectés incluent les séries Mk2, Mk3, Mk4, Mk5 et Q (versions antérieures aux correctifs répertoriés).

### Vulnérabilité
*   **Nature :** Erreur d'implémentation du RNG (générateur de nombres aléatoires) conduisant à une entropie prévisible. 
*   **CVE :** Aucune CVE n'est explicitement mentionnée dans l'article, bien que le problème soit documenté par Block et Coinkite.

### Recommandations pour les utilisateurs
1.  **Mise à jour :** Installer immédiatement la version du firmware corrigée (4.2.0+ pour Mk2/Mk3, 5.6.0+ pour Mk4/Mk5, 1.5.0Q+ pour Q, et versions Edge correspondantes).
2.  **Migration :** La mise à jour ne sécurise pas une graine déjà compromise. Il est impératif de générer une **nouvelle graine** sur un appareil mis à jour et de transférer les fonds vers ce nouveau portefeuille.
3.  **Renforcement :** L'utilisation d'une phrase secrète (passphrase) BIP-39 robuste est fortement recommandée, bien qu'elle ne remplace pas la nécessité de migrer vers une nouvelle graine.
4.  **Méthode alternative :** Pour les futures générations de clés, l'utilisation de dés (méthode manuelle) reste une solution efficace et indépendante du firmware pour garantir l'entropie.

---
[Source](https://www.bleepingcomputer.com/news/security/coldcard-wallet-rng-flaw-likely-linked-to-88-million-bitcoin-theft/){:target="_blank"}
