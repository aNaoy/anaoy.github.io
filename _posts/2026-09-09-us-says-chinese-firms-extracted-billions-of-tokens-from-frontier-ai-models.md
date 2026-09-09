---
title: 'US says Chinese firms extracted billions of tokens from frontier AI models'
date: 2026-09-09
permalink: /posts/2026/09/09/us-says-chinese-firms-extracted-billions-of-tokens-from-frontier-ai-models/
tags:
- veille-cyber
- bleepingcomp
---
### Vol de propriété intellectuelle : le pillage massif des modèles d'IA américains par la Chine

Des agences américaines (CISA, NSA, FBI) ont révélé que six entreprises chinoises (DeepSeek, Moonshot AI, Alibaba, MiniMax, StepFun et Z.AI) utilisent des attaques par distillation industrielle pour copier les capacités de modèles d'IA de pointe (Anthropic, OpenAI, Google, xAI). En exploitant des millions de requêtes via des comptes frauduleux et des proxies, ces firmes extraient des milliards de jetons pour réduire leurs coûts de développement et accélérer leur propre compétitivité.

**Points clés :**
*   **Méthode :** Utilisation de la distillation d'IA détournée pour transférer les connaissances et la logique de modèles avancés vers des modèles « étudiants » moins coûteux.
*   **Tactiques d'évasion :** Distribution massive de requêtes via des réseaux de proxies, rotation automatisée des points d'accès pour contourner les restrictions géographiques et les limites d'utilisation, et extraction spécifique des raisonnements en chaîne (Chain-of-Thought).
*   **Vulnérabilités :** L'article ne mentionne pas de CVE spécifique, car il s'agit d'un abus de services API légitimes et non d'une faille logicielle traditionnelle. La vulnérabilité réside dans la difficulté à distinguer un usage intensif légitime d'une extraction automatisée.

**Recommandations pour les entreprises d'IA :**
*   **Renforcement de la détection :** Surveiller les comportements suspects tels que les nouveaux comptes atteignant immédiatement leurs limites, les accès multi-IP pour un même compte, ou l'inactivité humaine prolongée.
*   **Gestion des réponses :** Modifier dynamiquement les réponses fournies par l'IA lorsqu'une tentative de distillation est suspectée afin d'induire en erreur les systèmes d'extraction.
*   **Collaboration :** Partager les renseignements sur les menaces et les indicateurs de compromission (IoC) entre les acteurs du secteur pour harmoniser les défenses.

---
[Source](https://www.bleepingcomputer.com/news/security/us-says-chinese-firms-extracted-billions-of-tokens-from-frontier-ai-models/){:target="_blank"}
