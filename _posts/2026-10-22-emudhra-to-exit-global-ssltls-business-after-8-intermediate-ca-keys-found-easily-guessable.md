---
title: 'eMudhra to Exit Global SSL/TLS Business After 8 Intermediate CA Keys Found Easily Guessable'
date: 2026-10-22
permalink: /posts/2026/10/22/emudhra-to-exit-global-ssltls-business-after-8-intermediate-ca-keys-found-easily-guessable/
tags:
- veille-cyber
- hackernews
---
### eMudhra se retire du marché mondial du SSL/TLS suite à une compromission de clés

L'autorité de certification (AC) eMudhra a annoncé son retrait du marché mondial des certificats SSL/TLS après la découverte de faiblesses critiques dans sa hiérarchie de sécurité. Un chercheur a révélé que huit clés privées d'autorités de certification intermédiaires étaient extrêmement faibles (valeurs inférieures à 256), les rendant trivialement prévisibles.

**Points clés :**
* **Compromission :** Huit clés privées intermédiaires ont été jugées "faciles à deviner", dont six dédiées aux certificats TLS.
* **Conséquences :** Google Chrome et Mozilla Firefox ont cessé de faire confiance à la racine *emSign ECC Root CA - G3*. Environ 30 800 certificats actifs, principalement utilisés par le service InCommon, sont impactés.
* **Réaction :** eMudhra a entamé une sortie du secteur SSL/TLS mondial (qui ne représente qu'environ 1 % de ses revenus) tout en maintenant ses autres activités.
* **Manque de transparence :** Des incidents survenus en 2025 concernant des listes de révocation (CRL) invalides suggèrent que l'entreprise utilisait déjà des clés défectueuses, soulevant des doutes sur sa gestion des incidents passés.

**Vulnérabilités :**
* **Clés faibles :** Les huit clés privées n'étaient pas générées comme des nombres aléatoires robustes, permettant leur reconstitution immédiate. Aucun identifiant CVE n'est associé, car il s'agit d'une erreur de génération de clés cryptographiques par l'AC.

**Recommandations :**
* **Pour les administrateurs :** Les détenteurs de certificats émis sous la racine *emSign ECC Root CA - G3* doivent impérativement acquérir et installer de nouveaux certificats TLS provenant d'une hiérarchie PKI différente et reconnue par les navigateurs.
* **Migration :** Privilégier le basculement vers une autre autorité de certification tierce plutôt que de se contenter de la racine RSA (G1) d'eMudhra, dont la fiabilité globale est remise en question par les éditeurs de navigateurs.
* **Automatisation :** Vérifier les configurations des clients ACME, car le remplacement automatique des certificats peut nécessiter des interventions manuelles ou des mises à jour de paramètres lors du changement de hiérarchie.

---
[Source](https://thehackernews.com/2026/10/emudhra-to-exit-global-ssltls-business.html){:target="_blank"}
