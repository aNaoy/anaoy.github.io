---
title: 'eMudhra Revokes 8 More CAs It Previously Declared Unaffected by Key Compromise'
date: 2026-11-11
permalink: /posts/2026/11/11/emudhra-revokes-8-more-cas-it-previously-declared-unaffected-by-key-compromise/
tags:
- veille-cyber
- hackernews
---
### Révocation supplémentaire de certificats eMudhra suite à une faille critique

L'autorité de certification eMudhra a dû révoquer 8 autorités de certification (CA) intermédiaires supplémentaires après avoir découvert que ses clés privées avaient été exposées lors d'une cérémonie de génération de clés en avril 2025. Ces certificats, initialement jugés sécurisés, ont finalement été invalidés par mesure de précaution.

**Points clés :**
*   **Origine de la défaillance :** Un script Python utilisé pour transférer des clés entre différents modèles de HSM (Hardware Security Modules) a extrait les clés privées en mémoire vive.
*   **Vulnérabilité technique :** Pour 8 clés ECDSA, une erreur dans le script a tronqué les clés à un seul octet, les rendant extrêmement faibles. Pour 8 autres clés RSA, bien que non tronquées, leur manipulation hors du HSM contrevient aux règles de sécurité, rendant impossible la garantie de leur intégrité.
*   **Conséquences :** 195 certificats ont été émis via ces infrastructures, incluant des certificats de sites web (TLS) et de signature de code. Bien qu'aucune utilisation malveillante ne soit confirmée, les clés exposées auraient théoriquement permis d'usurper l'identité de sites web.
*   **Fin d'activité :** eMudhra a annoncé son retrait du marché des certificats TLS mondialement reconnus. Le support de ses racines (G1) est progressivement supprimé par les éditeurs de navigateurs (Microsoft, Apple, Google/Mozilla).

**Vulnérabilités :**
*   **Défaut de contrôle des processus (Process Control Failure) :** Absence de test de robustesse des clés générées lors de la cérémonie.
*   **Manipulation de clés en mémoire (Key Material Exposure) :** Le script a fait transiter des clés privées dans la mémoire d'un ordinateur non sécurisé, violant la norme CPS §6.2.6.

**Recommandations :**
*   **Pour les détenteurs de certificats :** Identifier si leurs certificats sont liés aux émetteurs révoqués via les logs de *Certificate Transparency*.
*   **Migration :** Les organisations utilisant des certificats « emSign » doivent migrer vers un autre fournisseur de services de confiance immédiatement, étant donné la perte de confiance globale dans les racines eMudhra.
*   **Audit et conformité :** Renforcer les contrôles lors des cérémonies de génération de clés, notamment en interdisant le traitement des clés privées par des scripts personnalisés non audités et en garantissant que les clés ne quittent jamais l'environnement sécurisé des HSM.

---
[Source](https://thehackernews.com/2026/11/emudhra-revokes-8-more-cas-it.html){:target="_blank"}
