---
title: 'Two Critical Wasmtime Flaws Could Let Malicious WebAssembly Modules Escape Sandboxes'
date: 2026-10-26
permalink: /posts/2026/10/26/two-critical-wasmtime-flaws-could-let-malicious-webassembly-modules-escape-sandboxes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Wasmtime : risque d'évasion de sandbox

Deux failles critiques découvertes dans le moteur d'exécution WebAssembly Wasmtime permettent à un module malveillant de s'échapper de son environnement isolé (sandbox) pour exécuter du code arbitraire sur l'hôte. Ces vulnérabilités, présentes dans le compilateur Cranelift, ont reçu un score CVSS de 9,9/10.

**Points clés :**
* **Impact :** Les attaques nécessitent qu'un utilisateur puisse fournir ou compiler son propre module WebAssembly. Le risque est maximal pour les plateformes hébergeant du code tiers.
* **Mécanisme :**
    * **CVE-2026-115889 :** Un débordement d'entier lors de la gestion des valeurs internes peut provoquer une confusion de type.
    * **CVE-2026-115893 :** Spécifique à l'architecture **ARM64**, cette faille affecte l'instruction `br_table`, permettant un saut vers une adresse mémoire arbitraire via une manipulation de table de saut.
* **Historique :** Aucune exploitation active n'a été signalée à ce jour, mais la faille ARM64 existe depuis 2020.

**Recommandations :**
* **Mise à jour immédiate :** Passer aux versions corrigées (36.0.19, 48.0.7, 49.0.4 ou 50.0.0).
* **Reconstruction logicielle :** Comme Wasmtime est intégré sous forme de bibliothèque, il ne suffit pas de mettre à jour l'outil en ligne de commande ; chaque application utilisant Wasmtime doit être reconstruite avec la version corrigée.
* **Gestion du cycle de vie :** Les versions non supportées (notamment celles antérieures à la série 36.x LTS) ne recevant pas de correctifs, une montée de version majeure est impérative pour les utilisateurs sur ces branches obsolètes.

---
[Source](https://thehackernews.com/2026/10/two-critical-wasmtime-flaws-could-let.html){:target="_blank"}
