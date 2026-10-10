---
title: 'The Third-Party Agent Problem: Why Security Built for AI You Chose Misses the Agents You Didnt'
date: 2026-10-10
permalink: /posts/2026/10/10/the-third-party-agent-problem-why-security-built-for-ai-you-chose-misses-the-agents-you-didnt/
tags:
- veille-cyber
- hackernews
---
### Sécuriser l'écosystème invisible des agents IA tiers

La prolifération des agents IA intégrés nativement aux logiciels d'entreprise crée un angle mort majeur pour la cybersécurité. Contrairement aux outils IA traditionnels, ces agents sont souvent déployés sans décision formelle, échappant aux infrastructures d'identité classiques et aux contrôles de gouvernance habituels.

**Points clés :**
*   **Origines multiples :** Les agents sont soit « hérités » (via des mises à jour logicielles), « configurés » (prompts personnalisés), ou « construits » (frameworks open source). Les deux premières catégories dominent et sont invisibles aux outils de scan traditionnels.
*   **Risque lié à l'échafaudage :** Le danger ne réside pas dans le modèle de langage lui-même, mais dans son « échafaudage » (scaffolding) : ses permissions, ses accès aux données et ses capacités d'action sur d'autres systèmes.
*   **Propriété de connectivité :** La sécurité des agents ne peut plus être évaluée de manière isolée. Il faut analyser le « rayon d'action » (blast radius) de l'agent au sein de l'écosystème interconnecté de l'entreprise.

**Vulnérabilités :**
*   **Absence d'inventaire :** Impossible de sécuriser des agents non répertoriés par les équipes IT.
*   **Héritage excessif de privilèges :** Les agents héritent souvent des droits OAuth ou des rôles utilisateur sans restriction préalable (« par défaut »).
*   **Accès transitif :** Capacité d'un agent à rebondir d'un système à un autre (ex: de Slack vers un entrepôt de données puis vers un outil de ticketing), augmentant exponentiellement la surface d'exposition.
*   *Note : Aucune CVE spécifique n'est mentionnée, car il s'agit d'un problème structurel et systémique lié à l'architecture des applications modernes.*

**Recommandations :**
*   **Répondre aux quatre questions fondamentales :**
    1.  **Propriété :** Qui est le responsable humain désigné pour cet agent ?
    2.  **Autorisations :** Quels sont les privilèges (scopes) hérités et sont-ils strictement nécessaires ?
    3.  **Connectivité (Rayon d'action) :** Quelles sont les ressources accessibles directement et indirectement ?
    4.  **Comportement :** L'activité observée est-elle cohérente avec l'usage prévu, indépendamment de sa description théorique ?
*   **Adopter une vision holistique :** Passer d'une analyse ponctuelle à une cartographie continue des identités et des actions, liant humains, agents et applications.
*   **Appliquer le principe du moindre privilège :** Assigner aux agents une identité propre avec des privilèges nuls par défaut avant toute validation par les équipes de sécurité.

---
[Source](https://thehackernews.com/2026/10/the-third-party-agent-problem-why.html){:target="_blank"}
