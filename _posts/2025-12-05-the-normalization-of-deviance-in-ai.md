---
title: 'The Normalization of Deviance in AI'
date: 2025-12-05
permalink: /posts/2025/12/05/the-normalization-of-deviance-in-ai/
tags:
- veille-cyber
- zerodaysfans
---
**L'IA, Entre Progrès et Normalisation du Risque**

L'industrie de l'intelligence artificielle pourrait reproduire les erreurs culturelles ayant conduit à la catastrophe de la navette spatiale Challenger en normalisant progressivement les signaux d'alerte au nom du progrès. Ce phénomène, qualifié de "normalisation de la déviance", se manifeste par une dépendance excessive envers les sorties des modèles de langage, en particulier dans les systèmes autonomes. Ces modèles, intrinsèquement peu fiables et imprévisibles, exigent que les contrôles de sécurité soient appliqués en aval de leurs résultats.

Les exemples concrets incluent les systèmes qui autorisent des actions potentiellement critiques à partir de sorties LLM non fiables. Les défaillances, même bénignes comme les hallucinations ou les pertes de contexte, finissent par être acceptées comme normales. Le danger s'intensifie lorsque des entrées malveillantes, telles que les injections de prompts, exploitent cette complaisance culturelle. Des incidents tels que l'effacement de disques durs, la création d'issues GitHub aléatoires ou la suppression de bases de données de production témoignent déjà des conséquences de cette confiance aveugle. De plus, la recherche montre qu'une petite quantité de données empoisonnées peut introduire des portes dérobées dans les modèles, ouvrant la voie à des attaques généralisées.

Cette dérive culturelle s'opère par des raccourcis temporaires qui deviennent la nouvelle norme, souvent sous la pression de la concurrence, de la recherche d'économies et de l'enthousiasme général. Les entreprises, telles que Microsoft, OpenAI, Anthropic et Google, reconnaissent ces risques dans leurs documentations, mais la précipitation dans le déploiement de nouvelles fonctionnalités semble l'emporter sur les impératifs de sécurité fondamentale.

**Points Clés:**

*   **Normalisation de la Déviance en IA:** La tendance à accepter les sorties imparfaites ou dangereuses des LLM comme normales, au détriment de la sécurité.
*   **LLM comme Acteurs Non Fiables:** Les modèles de langage sont intrinsèquement imprévisibles et peuvent échouer à suivre les instructions de manière cohérente.
*   **Risques de Sécurité:** Les systèmes sont vulnérables aux attaques (injection de prompts) et aux défaillances intrinsèques des LLM (hallucinations, perte de contexte).
*   **Dérive Culturelle:** La normalisation se produit par une série de compromis acceptés, souvent sous la pression concurrentielle.

**Vulnérabilités (avec CVE si possible):**

*   **Injection de Prompts (Indirects et Directs):** Permet à des attaquants de manipuler les LLM pour exécuter des actions non désirées. Bien que des exemples spécifiques de CVE ne soient pas mentionnés pour chaque cas, le concept est clairement établi dans la littérature en cybersécurité concernant les LLM. Des recherches comme celles du "Month of AI Bugs" mettent en évidence ces problèmes récurrents.
*   **Empoisonnement de Modèles (Model Poisoning):** Des données malveillantes insérées pendant l'entraînement peuvent créer des portes dérobées. Les recherches d'Anthropic mentionnent que peu de documents suffisent à cet effet.
*   **Exfiltration de Données:** Les LLM peuvent être incités à envoyer des informations sensibles à des tiers malveillants.
*   **Exécution de Code à Distance (Remote Code Execution):** Les agents IA peuvent être utilisés pour exécuter du code arbitraire.

**Recommandations:**

*   **Sécurité en Aval:** Mettre en œuvre des contrôles de sécurité (vérifications d'accès, encodage, nettoyage) après la sortie des LLM.
*   **Modélisation des Menaces et Contrôles d'Accès:** Mener une modélisation approfondie des risques et mettre en place des mécanismes de contrôle robustes (sandbox, environnements hermétiques, principe de moindre privilège, identifiants temporaires).
*   **Surveillance Humaine:** Maintenir une supervision humaine, particulièrement dans les contextes à enjeux élevés.
*   **Réalisme sur les Capacités:** Adopter une approche réaliste quant aux capacités réelles des LLM et aux mécanismes de contrôle nécessaires.
*   **"Assume Breach":** Adopter une posture de sécurité où l'on présume qu'une violation finira par se produire.
*   **"Trust No AI":** Ne pas faire confiance aveuglément aux systèmes d'IA, mais plutôt les vérifier et les sécuriser rigoureusement.

---
[Source](https://embracethered.com/blog/posts/2025/the-normalization-of-deviance-in-ai/){:target="_blank"}
