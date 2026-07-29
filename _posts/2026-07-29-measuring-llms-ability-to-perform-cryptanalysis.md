---
title: 'Measuring LLMs’ Ability to Perform Cryptanalysis'
date: 2026-07-29
permalink: /posts/2026/07/29/measuring-llms-ability-to-perform-cryptanalysis/
tags:
- veille-cyber
- schneier
---
### Évaluation des capacités des modèles de langage en cryptanalyse

Le benchmark *CryptanalysisBench* a été introduit pour mesurer la capacité des grands modèles de langage (LLM) à concevoir des attaques cryptographiques. En évaluant 191 tâches sur divers algorithmes, cette étude démontre que les modèles de pointe (Claude, GPT, GLM) maîtrisent désormais la cryptanalyse mathématique, allant jusqu'à découvrir des vulnérabilités inédites.

**Points clés :**
*   **Performance accrue :** Les modèles actuels réussissent à casser 65 % à 86 % des schémas cryptographiques ayant des failles connues et parviennent à identifier des failles dans des systèmes complexes.
*   **Découvertes inédites :** Des modèles ont généré de nouvelles attaques, notamment contre l'algorithme SpoC AEAD et ont invalidé une preuve de sécurité CCA pour KINDI.
*   **Utilisation pratique :** Anthropic a utilisé ces méthodes pour identifier des faiblesses dans les protocoles Hawk et certaines versions d'AES.
*   **Finalité :** L'outil sert de banc d'essai pour tester la robustesse des nouveaux algorithmes avant leur déploiement à grande échelle.

**Vulnérabilités identifiées :**
*   **SpoC AEAD :** Exploitation d'un défaut de conception permettant la récupération de clés.
*   **KINDI :** Erreur logique dans la preuve de sécurité CCA (Chosen Ciphertext Attack).
*   **Hawk et AES (versions réduites) :** Faiblesses structurelles détectées par le modèle *Mythos Preview*.
*(Note : Aucune référence CVE n'est associée à ces découvertes dans le rapport initial).*

**Recommandations :**
*   **Stress-test systématique :** Utiliser *CryptanalysisBench* comme étape de validation obligatoire pour tout nouveau schéma cryptographique avant sa standardisation ou son implémentation.
*   **Veille technologique :** Surveiller étroitement l'évolution des capacités des LLM, qui pourraient bientôt égaler ou surpasser l'état de l'art humain en cryptanalyse.

---
[Source](https://www.schneier.com/blog/archives/2026/07/measuring-llms-ability-to-perform-cryptanalysis.html){:target="_blank"}
