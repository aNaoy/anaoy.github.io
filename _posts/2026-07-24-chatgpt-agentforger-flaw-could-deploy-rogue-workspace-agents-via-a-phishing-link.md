---
title: 'ChatGPT AgentForger Flaw Could Deploy Rogue Workspace Agents via a Phishing Link'
date: 2026-07-24
permalink: /posts/2026/07/24/chatgpt-agentforger-flaw-could-deploy-rogue-workspace-agents-via-a-phishing-link/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité AgentForger : Exploitation malveillante d'agents autonomes ChatGPT

Une faille de sécurité critique, baptisée **AgentForger**, a été identifiée dans l'outil de création d'agents (Agent Builder) de ChatGPT. Elle permettait à un attaquant de déployer un agent IA autonome au sein de l'environnement professionnel d'une victime via un simple lien de phishing. OpenAI a corrigé cette vulnérabilité le 8 juin 2026.

**Points clés :**
*   **Mécanisme d'attaque :** La faille repose sur une injection via les paramètres d'URL (`initial_assistant_prompt`). Lorsqu'une victime authentifiée clique sur un lien piégé, l'outil Agent Builder exécute automatiquement les instructions malveillantes contenues dans l'URL.
*   **Impact :** L'attaquant peut créer un agent, désactiver les approbations requises pour les connecteurs (Outlook, Gmail, Slack, etc.), et automatiser l'exécution de tâches (exfiltration de données, espionnage, phishing interne) sans interaction supplémentaire de la victime.
*   **Persistance :** Une fois configuré, l'agent peut fonctionner en arrière-plan de manière autonome, recevant des instructions directement via la boîte mail de la victime pour mener des opérations malveillantes sur le long terme.

**Vulnérabilités :**
*   **Type :** Cross-Site Request Forgery (CSRF) / Injection de commandes via paramètres URL.
*   **CVE :** Aucune CVE spécifique n'est mentionnée pour *AgentForger*, bien que l'article souligne une tendance aux abus d'infrastructure IA liée à d'autres failles (ex: CVE-2024-6587, CVE-2026-40217, CVE-2026-35029).

**Recommandations :**
*   **Mise à jour :** S'assurer que les outils OpenAI sont maintenus à jour (OpenAI a déjà déployé un correctif pour cette faille).
*   **Transition technologique :** Migrer vers le SDK Agents d'OpenAI, car l'outil "Agent Builder" sera officiellement déprécié le 30 novembre 2026.
*   **Hygiène de sécurité :** Sensibiliser les utilisateurs aux risques liés aux liens provenant de sources non vérifiées, même sur des plateformes SaaS d'entreprise, et surveiller les autorisations accordées aux connecteurs tiers au sein des outils d'IA.

---
[Source](https://thehackernews.com/2026/07/chatgpt-agentforger-flaw-could-deploy.html){:target="_blank"}
