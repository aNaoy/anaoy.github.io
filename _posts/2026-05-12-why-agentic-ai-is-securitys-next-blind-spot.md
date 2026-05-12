---
title: 'Why Agentic AI Is Securitys Next Blind Spot'
date: 2026-05-12
permalink: /posts/2026/05/12/why-agentic-ai-is-securitys-next-blind-spot/
tags:
- veille-cyber
- hackernews
---
### L'Intelligence Artificielle Agentique : Le prochain angle mort de la cybersécurité

L'adoption rapide de l'IA agentique (agents capables d'exécuter des tâches et de prendre des décisions de manière autonome) crée un risque majeur pour les entreprises. Les équipes de sécurité, faute de compréhension technique approfondie, sont souvent contournées par les unités métier, ce qui entraîne une exposition accrue sans contrôles adéquats.

**Points clés :**
*   **Perte de contrôle :** La démocratisation de la création d'agents permet à n'importe quel employé de concevoir des outils automatisés, créant un problème de « chaîne d'approvisionnement » interne non supervisé.
*   **Surface d'attaque étendue :** Les agents disposent de permissions larges (accès aux fichiers, emails, terminaux) nécessaires à leur efficacité, mais qui augmentent drastiquement le rayon d'impact en cas de compromission.
*   **Risque des protocoles d'intégration :** L'usage du *Model Context Protocol* (MCP) permet aux agents d'interagir avec des services externes, ouvrant la porte à des attaques par injection (ex: instructions cachées dans une invitation de calendrier).

**Vulnérabilités identifiées :**
*   **Injection de prompts via des canaux tiers :** Exploitation des données entrantes (emails, calendrier) pour manipuler le comportement de l'agent.
*   **Mouvements latéraux :** Un agent compromis peut servir de passerelle pour accéder à des systèmes sensibles ou exécuter du code arbitraire si les permissions ne sont pas cloisonnées.
*   **Absence de cloisonnement (Scope) :** Trop d'agents disposent de privilèges excessifs par rapport à leur fonction réelle.

**Recommandations :**
*   **S'approprier la technologie :** Les équipes de sécurité doivent expérimenter concrètement le développement d'agents pour comprendre leur architecture et leurs points de défaillance.
*   **Privilégier le « Security by Configuration » :** Appliquer le principe du moindre privilège en limitant strictement l'accès des agents à leurs seules fonctions nécessaires (ex: empêcher un agent de gestion de calendrier d'accéder à un terminal).
*   **Engagement précoce :** Intégrer la sécurité dès la conception des flux de travail automatisés plutôt que d'intervenir a posteriori.
*   **Veille active :** Suivre les cadres de menace émergents (comme ceux de l'OWASP) pour distinguer les solutions de sécurité réellement efficaces des simples arguments marketing.

---
[Source](https://thehackernews.com/2026/05/why-agentic-ai-is-securitys-next-blind.html){:target="_blank"}
