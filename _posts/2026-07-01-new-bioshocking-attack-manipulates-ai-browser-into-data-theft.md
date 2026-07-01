---
title: 'New BioShocking attack manipulates AI browser into data theft'
date: 2026-07-01
permalink: /posts/2026/07/01/new-bioshocking-attack-manipulates-ai-browser-into-data-theft/
tags:
- veille-cyber
- bleepingcomp
---
### BioShocking : La menace par injection de prompt sur les navigateurs IA

L'attaque « BioShocking », découverte par les chercheurs de LayerX, exploite une faille critique dans les navigateurs dotés d'agents IA. En utilisant une mise en situation ludique (type jeu vidéo), l'attaque conditionne l'agent IA à ignorer ses règles de sécurité, le conduisant à exécuter des actions malveillantes dans le monde réel, comme le vol de données sensibles (mots de passe, code source).

**Points clés :**
*   **Vulnérabilité conceptuelle :** Les agents IA peinent à distinguer les interactions dans un contexte fictif (jeu) des opérations réelles et sécurisées.
*   **Test de preuve de concept (PoC) :** Six navigateurs/outils IA (ChatGPT Atlas, Comet, Fellou, Genspark, Sigma, et le plugin Chrome Claude) ont été testés ; tous ont échoué à bloquer l'exfiltration de données lors du test.
*   **Réponse des éditeurs :** Seul OpenAI a déployé un correctif efficace. Les autres éditeurs ont soit ignoré le signalement, soit proposé un correctif jugé inefficace (Anthropic) ou fermé le rapport sans action (Perplexity AI).
*   **CVE :** Aucune CVE spécifique n'a été attribuée à ce jour, car il s'agit d'une vulnérabilité liée à la logique de conception des agents (injection de prompt/manipulation contextuelle).

**Recommandations :**
*   **Pour les éditeurs :**
    *   Imposer une confirmation explicite de l'utilisateur avant toute action sensible.
    *   Renforcer les vérifications de contexte et instaurer des limites de portée (scope) pour les sessions des agents.
*   **Pour les utilisateurs :**
    *   Restreindre manuellement les autorisations d'accès des navigateurs IA aux services et sites contenant des informations sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/new-bioshocking-attack-manipulates-ai-browser-into-data-theft/){:target="_blank"}
