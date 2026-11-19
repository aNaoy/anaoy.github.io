---
title: '30 Years of Gatekeeper Asymmetry Doom: The Paradox that Makes Powerful LLMs More Vulnerable'
date: 2026-11-19
permalink: /posts/2026/11/19/30-years-of-gatekeeper-asymmetry-doom-the-paradox-that-makes-powerful-llms-more-vulnerable/
tags:
- veille-cyber
- zerodaysfans
---
# Le principe de "Gatekeeper Asymmetry Doom"

Le concept de **Gatekeeper Asymmetry Doom** postule qu'un système de filtrage (le "portier") est condamné à l'échec s'il possède strictement moins de puissance de traitement que le système cible qu'il tente de protéger, sans s'appuyer sur des problèmes mathématiques complexes (cryptographie). Dès que le système de traitement a une capacité supérieure à celle du mécanisme de vérification, des contournements deviennent inévitables.

### Points clés
*   **Asymétrie de pouvoir :** L'écart de puissance entre le filtrage et l'exécution finale est la source fondamentale des failles de sécurité.
*   **Inévitabilité :** Plus la cible est complexe (ex: exécution Turing-complète), plus le portier (ex: liste de hachage, Regex, LLM léger) devient obsolète face à des vecteurs d'attaque polymorphes ou obfusqués.
*   **Donkeyspace :** La sécurité n'est pas un jeu à somme nulle ou un problème parfaitement résolu. L'objectif est de réduire la surface d'attaque en comprenant la position de l'attaquant dans un espace de stratégies sous-optimales.
*   **Rôle des LLM :** Bien que les LLM puissent aider à réduire cet écart de puissance, ils sont eux-mêmes soumis à ce principe : un LLM léger de "sanity check" sera toujours vulnérable face à un LLM cible plus puissant.

### Vulnérabilités notables citées
*   **Log4Shell (CVE-2021-44228) :** L'usage de listes de blocage (deny lists) basées sur des sous-chaînes a échoué face à des techniques d'obfuscation dynamiques exploitant la logique interne de l'application cible.
*   **Contournements de Sandboxes :** Utilisation de différences environnementales (ex: détection de mouvements de souris humains) pour identifier si le binaire est analysé dans un environnement contrôlé, rendant la sandbox aveugle.
*   **PuzzleMask :** Technique de prompt-crafting permettant à un payload malveillant de traverser un LLM de filtrage léger pour être exécuté par un LLM plus puissant qui, par son "intelligence" accrue, extrait et exécute le contenu malveillant.

### Recommandations
1.  **Réduire l'écart de pouvoir :** Améliorer la puissance du portier en intégrant des outils d'analyse plus profonds (code execution, raisonnement avancé) au sein même du processus de filtrage.
2.  **Approche pragmatique :** Ne pas chercher la perfection absolue, mais "serrer" la fenêtre de vulnérabilité. Même si le contournement est théoriquement possible, le rendre coûteux ou complexe améliore la sécurité réelle.
3.  **Défense en profondeur :** Puisque le "doom" est inévitable à long terme, prévoir systématiquement des plans de remédiation post-compromission.
4.  **Audit des surfaces :** Évaluer si une surface d'attaque est "condamnée" (doomed) et privilégier des mécanismes de défense qui, par nature, égalent ou dépassent la puissance du système protégé.

---
[Source](https://research.checkpoint.com/2026/30-years-of-gatekeeper-asymmetry-doom-the-paradox-that-makes-powerful-llms-more-vulnerable/){:target="_blank"}
