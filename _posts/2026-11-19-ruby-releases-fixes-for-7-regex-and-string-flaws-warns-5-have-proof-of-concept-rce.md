---
title: 'Ruby Releases Fixes for 7 Regex and String Flaws, Warns 5 Have Proof-of-Concept RCE'
date: 2026-11-19
permalink: /posts/2026/11/19/ruby-releases-fixes-for-7-regex-and-string-flaws-warns-5-have-proof-of-concept-rce/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Ruby : Correction de 7 failles de sécurité

Ruby a publié des mises à jour correctives pour sept failles de sécurité affectant son moteur d'expressions régulières (Regexp) et ses fonctions de conversion de casse des chaînes de caractères. Cinq de ces vulnérabilités disposent de preuves de concept (PoC) permettant potentiellement l'exécution de code à distance (RCE).

**Points clés :**
*   **Gravité :** 3 vulnérabilités sont classées "Critiques", 3 "Élevées" et 1 "Modérée".
*   **Risque :** L'exploitation dépend de la capacité d'un attaquant à injecter des chaînes ou des expressions régulières malveillantes traitées par l'application. Aucune exploitation active n'a été signalée à ce jour.
*   **Mise à jour :** Les correctifs sont disponibles dans les versions **4.0.10, 3.4.13 et 3.3.14**. Les versions antérieures à 3.3 ne sont plus supportées.

**Vulnérabilités identifiées (IDs GitHub) :**
*   **Critiques (RCE possible) :**
    *   `GHSA-34m4-m9fh-gqp5` : Débordement de tampon (heap overflow) lors de conversions de casse.
    *   `GHSA-7x2q-68qv-6p8x` : Double libération mémoire (double free) lors de la compilation de regex.
    *   `GHSA-3p8q-wmhx-vm2w` : Débordement de tampon lors de la compilation de regex.
*   **Élevées (RCE possible) :**
    *   `GHSA-87fm-7w84-j2px` : Débordement de tampon (résultat > 4 GiB).
    *   `GHSA-7whj-cfh7-xgm4` : Débordement de tampon via `Regexp#to_s`.
    *   `GHSA-wpqw-5qxg-m68r` : Lecture hors limites (out-of-bounds read) lors de correspondances insensibles à la casse.
*   **Modérée :**
    *   `GHSA-pvgc-g7gj-pv6h` : Lecture hors limites pouvant mener à une fuite de mémoire ou un crash.

**Recommandations :**
1.  **Mise à jour immédiate :** Mettre à jour l'interpréteur Ruby vers les versions corrigées (4.0.10, 3.4.13 ou 3.3.14). 
2.  **Redéploiement :** Une simple mise à jour des dépendances (gems) ne suffit pas ; il est impératif de mettre à jour l'interpréteur sur les serveurs d'application, les environnements d'exécution et de reconstruire les images de conteneurs.
3.  **Audit :** Vérifier les parties du code qui traitent des entrées utilisateur externes pour la construction d'expressions régulières ou la manipulation de chaînes de caractères (conversion de casse).
4.  **Support :** Migrer les applications utilisant des versions de Ruby antérieures à 3.3 vers une branche activement supportée, les versions obsolètes ne recevant plus de correctifs de sécurité.

---
[Source](https://thehackernews.com/2026/11/ruby-releases-fixes-for-7-regex-and.html){:target="_blank"}
