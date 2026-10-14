---
title: 'Ledger asks sellers across Asia to halt sales after supply-chain attack'
date: 2026-10-14
permalink: /posts/2026/10/14/ledger-asks-sellers-across-asia-to-halt-sales-after-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque sur la chaîne d'approvisionnement des portefeuilles Ledger

Ledger a ordonné l'arrêt immédiat de la vente de ses portefeuilles matériels dans toute l'Asie du Sud-Est et à Hong Kong suite à la découverte de dispositifs compromis. Des enquêtes ont révélé que des appareils vendus par le revendeur « CryptoBilis » (et potentiellement d'autres points de vente comme Metapod ou MediaMarkt) ont été altérés physiquement pour voler les actifs des utilisateurs.

**Points clés :**
*   **Mode opératoire :** L'attaque consiste en l'ajout d'un microcontrôleur tiers (implant matériel) à l'intérieur du portefeuille.
*   **Exfiltration :** Le composant malveillant intercepte la phrase de récupération de 24 mots et l'envoie à une entité tierce via une connexion LTE autonome (utilisant une eSIM intégrée).
*   **Indétectabilité :** L'implant ne modifie ni l'élément sécurisé (Secure Element), ni le système d'exploitation de Ledger, rendant la fraude invisible pour les outils d'autodiagnostic de l'appareil.
*   **Réaction de l'industrie :** Trezor a annoncé le renforcement drastique de son réseau de distribution, prévoyant de révoquer ses partenariats avec les revendeurs tiers dès janvier 2027 pour limiter les risques liés à la chaîne d'approvisionnement.

**Vulnérabilités :**
*   **Attaque physique par injection (Supply-chain attack) :** Absence de CVE spécifique, car il s'agit d'une modification matérielle frauduleuse effectuée lors de la distribution (interception physique) et non d'une faille logicielle ou matérielle native de Ledger.

**Recommandations :**
*   **Achat direct :** Privilégiez exclusivement l'achat de vos portefeuilles sur le site officiel du fabricant.
*   **Vigilance sur la provenance :** Évitez d'acheter des portefeuilles matériels auprès de revendeurs tiers non certifiés ou dans des boutiques aéroportuaires si leur fiabilité n'est pas garantie par le constructeur.
*   **Suspicion :** En cas de doute sur l'intégrité physique de votre appareil, cessez immédiatement de l'utiliser et transférez vos fonds vers un portefeuille dont la provenance est sûre.

---
[Source](https://www.bleepingcomputer.com/news/security/ledger-asks-sellers-across-asia-to-halt-sales-after-supply-chain-attack/){:target="_blank"}
