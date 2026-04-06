---
title: 'Drift $280M crypto theft linked to 6-month in-person operation'
date: 2026-04-06
permalink: /posts/2026/04/06/drift-280m-crypto-theft-linked-to-6-month-in-person-operation/
tags:
- veille-cyber
- bleepingcomp
---
### Infiltration et détournement de 280 millions de dollars sur Drift Protocol

Le protocole d'échange décentralisé Drift a subi un vol de 280 millions de dollars, orchestré par le groupe nord-coréen UNC4736 (associé à Lazarus). L'attaque est le résultat d'une opération de social engineering de longue haleine menée sur six mois lors de conférences internationales, durant laquelle des attaquants ont infiltré l'écosystème en se faisant passer pour une société de trading quantitative.

**Points clés :**
*   **Mode opératoire :** Infiltration physique par des intermédiaires, suivie d'échanges techniques via Telegram pour gagner la confiance des contributeurs de Drift.
*   **Exécution :** Le vol a été réalisé en 12 minutes après l'obtention des pouvoirs administratifs du conseil de sécurité (Security Council).
*   **Attribution :** Le groupe UNC4736 (AppleJeus / Labyrinth Chollima) est fortement suspecté.

**Vulnérabilités exploitées (vecteurs suspectés) :**
*   **Compromission via outils de développement :** Utilisation d'un dépôt de code malveillant exploitant potentiellement des vulnérabilités dans VSCode ou Cursor pour permettre l'exécution silencieuse de code.
*   **Ingénierie sociale technique :** Installation d'une application malveillante via TestFlight, présentée comme un produit de portefeuille numérique.

**Recommandations :**
*   **Vigilance sur la chaîne d'approvisionnement logicielle :** Vérifier systématiquement l'intégrité des dépôts de code partagés par des tiers avant toute exécution, même dans un contexte de collaboration professionnelle.
*   **Sécurisation des environnements de développement :** Maintenir les IDE et outils (VSCode, extensions) à jour pour prévenir l'exécution de code malveillant.
*   **Prudence avec les applications tierces :** Ne pas installer d'applications ou de binaires (via TestFlight ou autres) provenant de sources externes non vérifiées, quel que soit le niveau de confiance accordé aux interlocuteurs.
*   **Hygiène opérationnelle :** Appliquer le principe du moindre privilège aux accès administratifs (multisig) et limiter le nombre de contributeurs possédant des droits de haut niveau sur les protocoles financiers.

---
[Source](https://www.bleepingcomputer.com/news/security/drift-280m-crypto-theft-linked-to-6-month-in-person-operation/){:target="_blank"}
