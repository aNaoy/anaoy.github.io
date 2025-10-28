---
title: 'Function Peekaboo: Crafting self masking functions using LLVM'
date: 2025-10-28
permalink: /posts/2025/10/28/function-peekaboo-crafting-self-masking-functions-using-llvm/
tags:
- veille-cyber
- zerodaysfans
---
**Function Peekaboo : Protection de fonctions par obfuscation dynamique**

Une nouvelle technique baptisée "Function Peekaboo" permet d'obscurcir dynamiquement des fonctions spécifiques dans les programmes C++. Le principe est d'intégrer le code de masquage directement dans le compilateur LLVM, transformant ainsi le processus de compilation.

**Points Clés :**

*   **LLVM comme fondation :** L'infrastructure de compilation LLVM est exploitée pour sa flexibilité et sa capacité à manipuler le code à un niveau intermédiaire (IR).
*   **Masquage à l'exécution :** Les fonctions ainsi protégées restent obscurcies jusqu'à leur appel. Une fois exécutées, elles sont temporairement démasquées avant d'être à nouveau masquées au retour.
*   **Modification du compilateur :** Le compilateur Clang, basé sur LLVM, est personnalisé pour insérer des prologues et épilogues personnalisés avant et après chaque fonction enregistrée.
*   **Nouveau format d'exécutable :** Les binaires générés contiennent deux sections personnalisées : `.funcmeta` pour les métadonnées (clé XOR, adresses et tailles de fonctions) et `.stub` pour le code d'entrée du programme.
*   **Gestion du cycle de vie des fonctions :** Un "handler" central gère le démasquage/masquage, la gestion de la mémoire avec `VirtualProtect` et la mise à jour des métadonnées.
*   **Phase d'initialisation :** Avant l'exécution normale du programme (CRT), une phase d'initialisation enregistre et masque toutes les fonctions désignées.
*   **Modification du backend LLVM :** Des passes personnalisées (X86RetModPass) sont ajoutées au backend LLVM pour gérer la suppression des instructions `ret` et l'insertion de sauts vers le handler. La classe `X86AsmPrinter` est modifiée pour émettre le code de prologue, d'épilogue et du handler.
*   **Injection du stub d'entrée :** Un script Python est utilisé pour ajouter la section `.stub` au fichier exécutable et rediriger le point d'entrée original vers ce stub. Ce stub orchestre la phase d'initialisation et masque le code avant le démarrage normal.

**Vulnérabilités et Recommandations :**

Bien que l'article ne mentionne pas directement de vulnérabilités spécifiques liées à "Function Peekaboo", la technique vise à renforcer la protection des binaires contre l'analyse statique et dynamique.

*   **Protection contre l'analyse statique :** Le masquage rend plus difficile l'ingénierie inverse des fonctions.
*   **Protection contre l'analyse dynamique :** Le démasquage à la volée peut compliquer le débogage et la surveillance du comportement des fonctions.

Les recommandations implicites résident dans l'adoption de telles techniques pour la protection du code propriétaire ou sensible. Il est toutefois important de noter que toute technique d'obfuscation peut potentiellement être contournée par des attaquants suffisamment motivés et outillés. Une défense efficace combine souvent plusieurs couches de sécurité.

**Aucune CVE spécifique n'est référencée dans l'article.**

---
[Source](https://www.mdsec.co.uk/2025/10/function-peekaboo-crafting-self-masking-functions-using-llvm/){:target="_blank"}
