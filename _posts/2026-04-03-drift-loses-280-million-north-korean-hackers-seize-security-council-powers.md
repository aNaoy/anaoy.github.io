---
title: 'Drift loses $280 million North Korean hackers seize Security Council powers'
date: 2026-04-03
permalink: /posts/2026/04/03/drift-loses-280-million-north-korean-hackers-seize-security-council-powers/
tags:
- veille-cyber
- bleepingcomp
---
### Vol de 280 millions de dollars sur le protocole Drift par des hackers nord-coréens

Le protocole DeFi Drift, basé sur la blockchain Solana, a subi un piratage majeur estimé entre 280 et 285 millions de dollars. L'attaque a été attribuée par des entreprises de sécurité blockchain (Elliptic, TRM Labs) à des acteurs nord-coréens, en raison de techniques de blanchiment et d'indicateurs on-chain caractéristiques du groupe Lazarus.

**Points clés :**
* **Nature de l'attaque :** Il ne s'agit pas d'une faille dans les smart contracts, mais d'une compromission des pouvoirs administratifs du "Conseil de sécurité" du protocole.
* **Mode opératoire :** Entre le 23 et le 30 mars, les attaquants ont obtenu l'approbation nécessaire (2/5 signatures multisig) auprès des membres du Conseil pour préparer des transactions malveillantes différées via des comptes "durable nonce".
* **Exécution :** Le 1er avril, les pirates ont déclenché les transactions pré-signées, leur permettant de s'octroyer les droits d'administration, de supprimer les limites de retrait et de vider les fonds.
* **Impact :** Les fonctions de dépôt, de prêt et de trading ont été gelées. Les fonds de l'assurance et le jeton DSOL restent sécurisés.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car le problème réside dans la gouvernance et le processus de validation multisig plutôt que dans le code logiciel. La vulnérabilité principale est le compromis des membres du Conseil de sécurité ou de leurs clés de signature.

**Recommandations :**
* **Renforcement de la gouvernance :** Revoir les procédures de validation multisig et la gestion des clés privées pour les accès administratifs.
* **Détection précoce :** Améliorer la surveillance des transactions en attente ou différées ("durable nonce accounts") qui présentent des signatures suspectes.
* **Réponse à incident :** Collaboration active avec les autorités et les plateformes d'échange pour geler les actifs volés, conformément à la stratégie actuelle de Drift.
* **Transparence :** Publication attendue d'un rapport post-mortem complet pour identifier comment les signatures ont été obtenues illégitimement.

---
[Source](https://www.bleepingcomputer.com/news/security/drift-loses-280-million-north-korean-hackers-seize-security-council-powers/){:target="_blank"}
