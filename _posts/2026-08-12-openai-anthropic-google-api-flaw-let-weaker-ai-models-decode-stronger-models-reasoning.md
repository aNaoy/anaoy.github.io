---
title: 'OpenAI, Anthropic, Google API Flaw Let Weaker AI Models Decode Stronger Models Reasoning'
date: 2026-08-12
permalink: /posts/2026/08/12/openai-anthropic-google-api-flaw-let-weaker-ai-models-decode-stronger-models-reasoning/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité majeure des traces de raisonnement dans les API d'IA

Une faille de conception dans les API d'OpenAI, Anthropic et Google permettait à des modèles d'IA moins puissants de « décoder » le raisonnement interne de modèles plus avancés. En exploitant la portabilité des blocs de raisonnement chiffrés, des attaquants pouvaient extraire des données sensibles contenues dans ces traces, même si elles étaient absentes du texte visible par l'utilisateur.

**Points clés :**
* **Mécanisme d'attaque :** Les blocs de raisonnement chiffrés (utilisés pour maintenir l'état de la session) n'étaient pas liés à un utilisateur ou une session spécifique. Ils pouvaient être rejoués et soumis à un modèle de la même famille (ex: Claude Haiku pour déchiffrer Claude) afin de reconstruire le contenu caché.
* **Impact des données :** L'analyse de 6 708 trajectoires d'agents publics a permis d'extraire 704 artefacts privés, dont 62 clés API, 33 mots de passe et 24 jetons d'accès.
* **Vecteurs d'abus :** La vulnérabilité permettait également la distillation de modèles, l'extraction de contenus malveillants cachés, et l'injection de prompts invisibles via des blocs de raisonnement opaques.
* **Statut actuel :** Selon les chercheurs, les attaques démontrées ne sont plus reproductibles depuis août 2026 grâce à des mesures d'atténuation non documentées officiellement par les fournisseurs.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été attribuée, car il s'agit d'une vulnérabilité de conception (logique de traitement des jetons de raisonnement) plutôt que d'un défaut de chiffrement.

**Recommandations :**
* **Nettoyage des traces :** Supprimer systématiquement les blocs de raisonnement et les champs opaques avant de publier ou de partager des journaux d'agents (logs).
* **Gestion des transcripts :** Ne jamais publier de transcriptions brutes d'API, même si le texte visible semble avoir été anonymisé.
* **Isolation :** En cas de changement de modèle au sein d'une même plateforme, les blocs de raisonnement hérités doivent être purgés, car ils peuvent être mal interprétés ou exploités.

---
[Source](https://thehackernews.com/2026/08/openai-anthropic-google-api-flaw-let.html){:target="_blank"}
