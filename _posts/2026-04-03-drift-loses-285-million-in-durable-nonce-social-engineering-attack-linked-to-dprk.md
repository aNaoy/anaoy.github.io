---
title: 'Drift Loses $285 Million in Durable Nonce Social Engineering Attack Linked to DPRK'
date: 2026-04-03
permalink: /posts/2026/04/03/drift-loses-285-million-in-durable-nonce-social-engineering-attack-linked-to-dprk/
tags:
- veille-cyber
- hackernews
---
### Attaque par ingénierie sociale contre Drift : 285 millions de dollars dérobés

La plateforme d'échange décentralisée Drift a subi une perte de 285 millions de dollars le 1er avril 2026 suite à une opération sophistiquée impliquant des mécanismes de « durable nonces » et une ingénierie sociale ciblée. Les investigations suggèrent une implication de pirates liés à la Corée du Nord (RPDC), un mode opératoire cohérent avec les attaques majeures observées précédemment dans le secteur Web3.

**Points clés :**
*   **Mode opératoire :** Les attaquants ont manipulé des signataires multi-signature (multisig) pour obtenir des pré-approbations de transactions frauduleuses sur plusieurs semaines.
*   **Détournement :** Une fois le contrôle administratif obtenu, les attaquants ont supprimé les limites de retrait et injecté un actif factice (« CarbonVote Token ») pour drainer les liquidités en moins de 10 secondes.
*   **Origine probable :** Les méthodologies de blanchiment et les indicateurs on-chain pointent vers des groupes étatiques nord-coréens, habitués à financer les programmes d'armement du régime via le vol massif d'actifs cryptographiques.

**Vulnérabilités exploitées :**
*   **Absence de faille logicielle :** Aucune vulnérabilité n'a été détectée dans les contrats intelligents. L'attaque a exploité une faille humaine et procédurale.
*   **Faille opérationnelle :** Utilisation de l'ingénierie sociale pour contourner la sécurité multisig et absence de « timelock » (délai d'exécution) lors de la migration du Conseil de Sécurité, supprimant la dernière ligne de défense.
*   *Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une compromission de processus administratifs.*

**Recommandations :**
*   **Renforcement de la gouvernance :** Implémenter des délais de sécurité (timelocks) systématiques pour toute modification des permissions critiques ou migration de privilèges administratifs.
*   **Sécurisation des processus multisig :** Mettre en place des protocoles stricts de vérification « hors-chaîne » pour toute signature, afin d'éviter la validation de transactions manipulées.
*   **Vigilance accrue :** Face à l'usage croissant de l'IA et de techniques de social engineering sophistiquées par des groupes comme UNC1069, les organisations doivent sensibiliser leurs contributeurs aux campagnes de phishing personnalisées.
*   **Analyse des actifs :** Renforcer la validation des oracles de prix pour éviter qu'une liquidité artificielle puisse être utilisée comme garantie pour des retraits massifs.

---
[Source](https://thehackernews.com/2026/04/drift-loses-285-million-in-durable.html){:target="_blank"}
