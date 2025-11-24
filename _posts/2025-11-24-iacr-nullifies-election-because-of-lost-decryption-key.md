---
title: 'IACR Nullifies Election Because of Lost Decryption Key'
date: 2025-11-24
permalink: /posts/2025/11/24/iacr-nullifies-election-because-of-lost-decryption-key/
tags:
- veille-cyber
- schneier
---
### Clé cryptographique perdue, élection annulée

L'Association Internationale de Recherche Cryptographique (IACR) a dû annuler une élection en ligne suite à la perte irréversible de sa clé de déchiffrement par l'un des trois administrateurs. Le système de vote Helios, conçu pour garantir la sécurité et la vérifiabilité, exigeait la combinaison des parts de clé de tous les administrateurs pour déchiffrer les résultats. L'erreur humaine d'un fiduciaire a rendu le processus de déchiffrement techniquement impossible, empêchant ainsi l'obtention et la vérification du résultat final. L'élection sera refaite, avec une modification du seuil de déchiffrement, passant d'un système à 3 sur 3 à un système 2 sur 3.

**Points Clés :**

*   Une élection en ligne organisée par l'IACR a été annulée.
*   La raison de l'annulation est la perte d'une clé de déchiffrement par un administrateur.
*   Le système de vote Helios exigeait la participation de trois administrateurs pour le déchiffrement.
*   L'erreur humaine a empêché le déchiffrement et la vérification des résultats.
*   Une nouvelle élection sera organisée avec un seuil de déchiffrement ajusté.

**Vulnérabilités :**

*   Aucune vulnérabilité technique ou faille logicielle spécifique (CVE) n'est mentionnée. Le problème découle d'une erreur opérationnelle (perte de clé) et non d'une faiblesse du système de chiffrement lui-même.

**Recommandations :**

*   Mettre en place des mécanismes de récupération ou de redondance pour les clés cryptographiques critiques.
*   Évaluer la robustesse des procédures de gestion des clés et envisager des solutions permettant de pallier la perte accidentelle d'une part de clé, tout en maintenant la sécurité.
*   Adapter les seuils de confiance (par exemple, passer d'un système N sur N à un système K sur N où K < N) pour accroître la résilience face à des défaillances individuelles.

---
[Source](https://www.schneier.com/blog/archives/2025/11/iacr-nullifies-election-because-of-lost-decryption-key.html){:target="_blank"}
