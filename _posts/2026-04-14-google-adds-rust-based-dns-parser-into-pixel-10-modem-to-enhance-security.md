---
title: 'Google Adds Rust-Based DNS Parser into Pixel 10 Modem to Enhance Security'
date: 2026-04-14
permalink: /posts/2026/04/14/google-adds-rust-based-dns-parser-into-pixel-10-modem-to-enhance-security/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité des modems Pixel via Rust

Google intègre un parseur DNS basé sur Rust dans le firmware du modem des appareils Pixel 10. Cette initiative marque une étape clé dans l'adoption de langages à mémoire sécurisée pour les composants système critiques, visant à réduire la surface d'attaque liée aux vulnérabilités mémoires.

**Points clés :**
*   **Adoption de Rust :** Utilisation de la bibliothèque `hickory-proto` (adaptée pour le bare metal) afin de sécuriser le protocole DNS, essentiel aux communications cellulaires modernes.
*   **Interopérabilité :** Le parseur utilise une interface en C pour communiquer avec les structures de données existantes du firmware, garantissant une intégration fluide avec le code source originel.
*   **Gestion des dépendances :** Introduction de l'outil `cargo-gnaw` pour faciliter la maintenance et la résolution des dépendances logicielles.
*   **Optimisation :** Google envisage l'utilisation de "feature flags" pour optimiser la taille du code dans les environnements contraints en mémoire.

**Vulnérabilités ciblées :**
*   L'implémentation vise à prévenir les erreurs de type accès mémoire hors limites (*out-of-bound memory accesses*), courantes dans les langages non sécurisés comme le C.
*   Référence spécifique : **CVE-2024-27227** (vulnérabilité liée à l'insécurité mémoire dans le parsing DNS).

**Recommandations :**
*   **Généralisation de la sécurité mémoire :** Poursuivre la transition des composants critiques du firmware vers Rust pour minimiser les risques de dépassement de tampon (*buffer overflows*) et d'exécution de code à distance.
*   **Modularité :** Adopter des techniques de compilation sélective pour limiter l'empreinte mémoire des bibliothèques tierces intégrées dans des systèmes embarqués.

---
[Source](https://thehackernews.com/2026/04/google-adds-rust-based-dns-parser-into.html){:target="_blank"}
