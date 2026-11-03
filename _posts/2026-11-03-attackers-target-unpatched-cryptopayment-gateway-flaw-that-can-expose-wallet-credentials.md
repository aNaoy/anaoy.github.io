---
title: 'Attackers Target Unpatched CryptoPayment Gateway Flaw That Can Expose Wallet Credentials'
date: 2026-11-03
permalink: /posts/2026/11/03/attackers-target-unpatched-cryptopayment-gateway-flaw-that-can-expose-wallet-credentials/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le plugin WordPress CryptoPayment Gateway

Des cyberattaquants exploitent activement une faille de sécurité critique dans le plugin WordPress **CryptoPayment Gateway** (versions 1.2.1 à 1.2.2). Le plugin a été retiré du répertoire officiel de WordPress en raison de cette vulnérabilité, pour laquelle aucun correctif n'est actuellement disponible.

**Points clés :**
*   **Nature de l'attaque :** Des attaquants non authentifiés peuvent exécuter des opérations administratives via un point de terminaison AJAX non protégé.
*   **Conséquences :** Suppression arbitraire de fichiers sur le serveur, écrasement de la configuration de la passerelle de paiement et récupération des identifiants de portefeuilles en texte clair.
*   **Infrastructure malveillante :** Les tentatives d'exploitation proviennent d'infrastructures proposant des services d'hébergement VPS anonymes sans KYC.

**Vulnérabilité identifiée :**
*   **CVE-2026-81648 :** Score CVSS de 10.0 (critique).

**Recommandations :**
*   **Suppression immédiate :** Désinstaller et supprimer complètement le plugin du site WordPress.
*   **Rotation des clés :** Renouveler immédiatement toutes les clés et identifiants de portefeuilles cryptographiques associés au plugin.
*   **Audit de sécurité :** Rechercher tout signe de compromission ou de modification suspecte dans les fichiers et les configurations du site web.

---
[Source](https://thehackernews.com/2026/11/attackers-target-unpatched.html){:target="_blank"}
