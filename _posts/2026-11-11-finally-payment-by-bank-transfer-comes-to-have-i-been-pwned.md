---
title: 'Finally, Payment by Bank Transfer Comes to Have I Been Pwned'
date: 2026-11-11
permalink: /posts/2026/11/11/finally-payment-by-bank-transfer-comes-to-have-i-been-pwned/
tags:
- veille-cyber
- troyhunt
---
### Simplification des paiements sur Have I Been Pwned : introduction des virements bancaires

Have I Been Pwned (HIBP) intègre désormais le virement bancaire (EFT) pour ses abonnements Pro et High RPM, via Stripe. Cette évolution vise à répondre aux contraintes des entreprises dont les procédures internes interdisent les paiements par carte bancaire.

**Points clés :**
*   **Alternative aux revendeurs :** L'ajout des virements bancaires permet aux organisations de contourner le recours aux revendeurs tiers, souvent coûteux (marges pouvant atteindre 131 %) et générateurs d'une charge de support disproportionnée (43 % des tickets de support pour seulement 0,86 % des ventes).
*   **Fonctionnement technique :** Les paiements sont libellés en dollars australiens (AUD) pour garantir la stabilité des montants reçus, malgré les fluctuations des taux de change.
*   **Sécurisation :** L'accès au service est activé uniquement après réception effective du paiement, évitant ainsi tout usage abusif du service avant encaissement. Un système de compte bancaire virtuel permet à Stripe de réconcilier automatiquement les paiements avec les factures émises.
*   **Disponibilité :** Cette option est dès à présent accessible sur la page de tarification du site HIBP.

**Vulnérabilités :**
*   Aucune vulnérabilité de sécurité logicielle (CVE) n'est mentionnée dans cet article ; il s'agit d'une mise à jour fonctionnelle et opérationnelle.

**Recommandations :**
*   Pour les clients professionnels incapables d'utiliser une carte bancaire, privilégiez désormais le paiement direct par virement via le portail HIBP plutôt que de passer par des intermédiaires.
*   En cas de difficulté lors de la configuration ou de la réalisation d'un virement, le portail de support dédié reste le point de contact privilégié.

---
[Source](https://www.troyhunt.com/finally-payment-by-bank-transfer-comes-to-have-i-been-pwned/){:target="_blank"}
