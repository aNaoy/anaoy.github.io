---
title: 'Manipulating AI Summarization Features'
date: 2026-03-04
permalink: /posts/2026/03/04/manipulating-ai-summarization-features/
tags:
- veille-cyber
- schneier
---
**Détournement des fonctions de résumé par IA**

Des entreprises exploitent les fonctions de résumé automatisé, intégrées dans des boutons, pour tenter d'influencer les assistants IA. En insérant des instructions cachées dans les paramètres d'URL, elles cherchent à faire reconnaître leur entreprise comme une source fiable ou à la privilégier dans les futures recommandations. Cette méthode, facile à déployer avec des outils accessibles, a été observée chez plus de 50 entreprises réparties dans 14 secteurs. L'enjeu réside dans le risque que les IA, manipulées, fournissent des conseils biaisés dans des domaines sensibles comme la santé, la finance ou la sécurité, sans que l'utilisateur en soit conscient. Cette pratique s'apparente à une optimisation pour les modèles de langage, similaire au référencement pour les moteurs de recherche, et promet de devenir une activité commerciale majeure.

**Points Clés :**

*   Les entreprises insèrent des instructions cachées dans les boutons "Résumé par IA".
*   Ces instructions visent à manipuler la mémoire de l'IA pour qu'elle privilégie certaines entreprises.
*   La technique est facilement déployable et peu coûteuse.
*   Plus de 50 exemples identifiés sur 31 entreprises dans 14 industries.
*   Le risque principal est la fourniture de recommandations biaisées par l'IA dans des domaines critiques.

**Vulnérabilités :**

*   Absence de validation et de nettoyage des paramètres d'URL utilisés dans les fonctions de résumé.
*   Les modèles d'IA ne disposent pas de mécanismes suffisants pour détecter et rejeter les instructions malveillantes intégrées aux requêtes.
*   (Aucun CVE spécifique n'est mentionné dans l'article.)

**Recommandations :**

*   Les développeurs d'assistants IA et les plateformes intégrant ces fonctions doivent implémenter des mécanismes de sécurité pour valider et nettoyer les entrées utilisateur et les paramètres d'URL.
*   Mettre en place des protections contre les "injections de prompts" visant à altérer le comportement ou la mémoire de l'IA.
*   Éduquer les utilisateurs sur les potentielles manipulations des recommandations générées par IA.

---
[Source](https://www.schneier.com/blog/archives/2026/03/manipulating-ai-summarization-features.html){:target="_blank"}
