---
title: 'Interesting Paper Exploring Prompt Injection'
date: 2026-06-25
permalink: /posts/2026/06/25/interesting-paper-exploring-prompt-injection/
tags:
- veille-cyber
- schneier
---
### La confusion des rôles : la faille fondamentale des LLM

L’étude « Prompt Injection as Role Confusion » démontre que les LLM ne parviennent pas à isoler réellement les instructions des données, malgré l'usage de balises de formatage. La vulnérabilité réside dans la nature même des modèles : ils interprètent les rôles comme des continuités stylistiques plutôt que comme des frontières logiques strictes.

**Points clés :**
*   **Échec de l'architecture :** Les balises de rôle (ex: système vs utilisateur) servent d'échafaudage cognitif mais disparaissent dans les représentations internes du modèle.
*   **Nature des attaques :** Les injections ne sont pas seulement des commandes directes, mais des manipulations de l'état du modèle via des changements subtils de style.
*   **Limites de la défense :** Tant que les LLM n'auront pas une perception réelle et autonome de leur rôle, les protections resteront inefficaces (« jeu du chat et de la souris »).

**Vulnérabilités :**
*   **Confusion de rôle (Role Confusion) :** Il ne s'agit pas d'une CVE spécifique, mais d'une faille systémique inhérente à l'architecture des grands modèles de langage. La porosité entre les instructions et les données permet le détournement du comportement du modèle par injection.

**Recommandations :**
*   **Recherche approfondie :** Étudier davantage les abstractions de « rôles » dans la pile technologique des LLM, car elles constituent la frontière entre la pensée du modèle et les données externes.
*   **Défense proactive :** Ne pas se reposer uniquement sur des filtres de balises, car le système est fondamentalement incapable de distinguer le « soi » de l'« autre » de manière rigide.
*   **Approche systémique :** Développer de nouvelles architectures qui permettent une perception authentique des limites de contexte, au-delà du simple formatage textuel.

---
[Source](https://www.schneier.com/blog/archives/2026/06/interesting-paper-exploring-prompt-injection.html){:target="_blank"}
