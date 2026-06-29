---
title: 'Why Post-Quantum Cryptography Starts With Credentials'
date: 2026-06-29
permalink: /posts/2026/06/29/why-post-quantum-cryptography-starts-with-credentials/
tags:
- veille-cyber
- hackernews
---
### Sécurisation post-quantique : Priorité aux identifiants

L'avènement de l'informatique quantique menace de rendre obsolètes les algorithmes de chiffrement actuels (RSA, ECC), permettant aux attaquants de déchiffrer des données interceptées aujourd'hui. Bien qu'un ordinateur quantique opérationnel soit estimé à 15 ans, la stratégie « Harvest Now, Decrypt Later » (intercepter maintenant, déchiffrer plus tard) rend la menace immédiate.

**Points clés :**
*   **Vulnérabilité des identifiants :** Contrairement aux données éphémères, les identifiants (mots de passe, clés API, comptes de service) ont une durée de vie longue, ce qui en fait les cibles privilégiées des attaquants.
*   **Échéances réglementaires :** La NSA et le NIST prévoient le retrait progressif de RSA-2048 et ECC P-256 d'ici 2030-2035, imposant une transition urgente vers des algorithmes résistants au quantique.
*   **Risque lié aux NHI :** La prolifération des identités non-humaines (NHI), souvent non inventoriées, augmente considérablement la surface d'exposition.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne la vulnérabilité intrinsèque de la cryptographie à clé publique actuelle (RSA/ECC) face aux algorithmes de factorisation quantique.

**Recommandations :**
*   **Inventaire exhaustif :** Identifier tous les systèmes gérant des secrets (gestionnaires de mots de passe, plateformes PAM) pour localiser les identifiants dormants ou codés en dur.
*   **Priorisation par le risque :** Se concentrer sur les secrets à longue durée de vie qui protègent des accès critiques plutôt que sur le volume total de données.
*   **Adoption de la cryptographie hybride :** Combiner les algorithmes classiques actuels avec des algorithmes résistants au quantique (ex: Kyber) pour assurer une protection immédiate sans abandonner les standards éprouvés.
*   **Conception pour l'agilité cryptographique :** Centraliser la gestion de la cryptographie pour permettre des mises à jour algorithmiques rapides via des changements de configuration, évitant ainsi des refontes majeures lors de futures évolutions technologiques.

---
[Source](https://thehackernews.com/2026/06/why-post-quantum-cryptography-starts.html){:target="_blank"}
