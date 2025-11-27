---
title: 'Popular Forge library gets fix for signature verification bypass flaw'
date: 2025-11-27
permalink: /posts/2025/11/27/popular-forge-library-gets-fix-for-signature-verification-bypass-flaw/
tags:
- veille-cyber
- bleepingcomp
---
**Faille dans une librairie cryptographique JavaScript : Contournement de la vérification des signatures**

Une vulnérabilité critique a été découverte dans la librairie JavaScript `node-forge`, largement utilisée pour ses fonctions de cryptographie et d'infrastructure à clé publique (PKI). Cette faille, référencée sous le nom de CVE-2025-12816, permet à des attaquants non authentifiés de contourner les mécanismes de vérification des signatures en créant des structures de données ASN.1 malformées qui semblent valides.

**Points clés :**
*   La librairie `node-forge` est extrêmement populaire, avec près de 26 millions de téléchargements hebdomadaires sur le registre NPM.
*   La vulnérabilité découle d'un conflit d'interprétation dans le mécanisme de validation ASN.1 de la librairie.
*   Des applications s'appuyant sur `node-forge` pour sécuriser des protocoles cryptographiques basés sur ASN.1 peuvent être trompées.
*   L'impact potentiel peut varier selon l'application, mais inclut le contournement d'authentification, la falsification de données signées et l'utilisation abusive de fonctions liées aux certificats.

**Vulnérabilités :**
*   **CVE-2025-12816** : Failledans le mécanisme de validation ASN.1 de `node-forge` (versions 1.3.1 et antérieures) permettant le contournement de la vérification des signatures.

**Recommandations :**
*   Les développeurs utilisant `node-forge` doivent mettre à jour vers la version 1.3.2 ou une version ultérieure dès que possible.

---
[Source](https://www.bleepingcomputer.com/news/security/popular-forge-library-gets-fix-for-signature-verification-bypass-flaw/){:target="_blank"}
