---
title: 'Signal’s Post-Quantum Cryptographic Implementation'
date: 2025-10-29
permalink: /posts/2025/10/29/signals-post-quantum-cryptographic-implementation/
tags:
- veille-cyber
- schneier
---
### Signal Renforce sa Sécurité avec une Cryptographie Post-Quantique

Signal a déployé une mise à jour majeure de son système de messagerie sécurisée en intégrant une implémentation cryptographique résistante aux ordinateurs quantiques. Cette évolution vise à assurer la confidentialité des communications face aux menaces futures.

L'approche adoptée par Signal consiste à superposer un nouveau mécanisme de chiffrement, nommé Sparse Post Quantum Ratchet (SPQR), à son système existant (le Double Ratchet classique). Le chiffrement d'un message combine désormais des clés issues des deux systèmes. Cette méthode permet d'obtenir une clé de chiffrement finale qui bénéficie de la sécurité du Double Ratchet traditionnel tout en étant protégée contre les attaques futures potentielles d'ordinateurs quantiques.

Cette innovation, développée en collaboration avec PQShield, AIST et l'Université de New York, a été présentée lors de conférences académiques telles qu'Eurocrypt 2025 et Usenix 25. L'équipe a évalué plusieurs options pour ajouter la sécurité post-quantique et la sécurité post-compromission, le système SPQR se démarquant parmi elles. Le protocole a également été adapté pour utiliser le standard ML-KEM, une partie du processus de normalisation post-quantique du NIST.

Le principal avantage de cette implémentation réside dans sa robustesse accrue. En combinant deux ratchets indépendants (un classique basé sur le Diffie-Hellman et un nouveau basé sur KEM), le système assure que même si l'un des deux mécanismes était compromis (par un ordinateur quantique, une faille dans les courbes elliptiques ou ML-KEM, ou une implémentation défectueuse), les messages resteraient protégés par le second. Cela revient, de manière simplifiée, à doubler la sécurité de la partie "ratchet" du protocole, offrant un bénéfice même pour les utilisateurs qui ne sont pas directement concernés par la menace quantique.

**Points Clés :**

*   Signal intègre une cryptographie post-quantique dans son protocole de messagerie.
*   Une approche hybride est utilisée : un nouveau ratchet résistant aux quantiques (SPQR) est ajouté au ratchet classique existant.
*   Les clés de chiffrement des deux ratchets sont mélangées pour former la clé finale.
*   Cette méthode assure la sécurité contre les ordinateurs quantiques tout en conservant les avantages du système actuel.
*   La solution apporte une sécurité accrue même en cas de compromission d'un des deux mécanismes.

**Vulnérabilités :**

*   L'article ne mentionne pas de vulnérabilités spécifiques (avec CVE) qui ont été corrigées, mais plutôt une anticipation des futures menaces posées par les ordinateurs quantiques.

**Recommandations :**

*   L'implémentation de Signal démontre une stratégie proactive pour la sécurité post-quantique, en combinant des mécanismes existants et nouveaux pour une résilience maximale.
*   L'adoption de standards comme ML-KEM est cruciale pour l'interopérabilité et la confiance dans la sécurité future.
*   La diversification des mécanismes cryptographiques renforce la sécurité globale et la capacité à résister à des attaques ciblées sur une technologie spécifique.

---
[Source](https://www.schneier.com/blog/archives/2025/10/signals-post-quantum-cryptographic-implementation.html){:target="_blank"}
