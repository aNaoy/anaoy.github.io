---
title: 'Google Deletes 3 ADK AI Workflows After Malicious GitHub Issue Could Trigger Privileged Agent'
date: 2026-08-04
permalink: /posts/2026/08/04/google-deletes-3-adk-ai-workflows-after-malicious-github-issue-could-trigger-privileged-agent/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des flux de travail AI : Google supprime trois agents du dépôt ADK

Des chercheurs de Pillar Security ont révélé une faille critique dans le dépôt Python « Agent Development Kit » (ADK) de Google, permettant à un attaquant de manipuler des agents IA via des injections de prompt. Google a par la suite supprimé trois flux de travail automatisés pour neutraliser le risque.

**Points clés :**
*   **Chaînage d'agents :** Un agent de tri public était vulnérable à une injection de prompt, permettant à un utilisateur malveillant de forcer le bot à poster une commande (`/adk-issue-fix`) reconnue par un agent privilégié.
*   **Usurpation d'identité :** Le système de sécurité se basait sur l'identité du bot (considéré comme « collaborateur ») pour autoriser les actions, sans vérifier si l'entrée initiale était fiable.
*   **Impact :** L'exploitation permettait l'exécution de code arbitraire sur le runner CI et l'exfiltration de jetons d'accès personnels (PAT), de clés API Google et d'identifiants de compte de service.
*   **Technique :** Bien que le runner restreignait les commandes aux outils `gh` ou `git`, l'agent pouvait utiliser des hooks Git malveillants (`core.hooksPath`) pour exécuter des payloads arbitraires.

**Vulnérabilités :**
*   **Injection de prompt (Prompt Injection) :** Manipulation du contenu public pour déclencher des actions privilégiées.
*   **Défaut de conception des privilèges :** Confusion entre l'identité du bot et l'origine non fiable de la requête.
*   **Escalade de privilèges CI/CD :** Utilisation d'outils autorisés (Git) pour contourner les restrictions de commandes et exécuter du code arbitraire.

**Recommandations :**
*   **Segmentation des identités :** Utiliser des identités de bots distinctes pour les tâches publiques et les tâches privilégiées.
*   **Principe du moindre privilège :** Restreindre strictement les permissions (scopes) des jetons (PAT) et des comptes de service au strict nécessaire.
*   **Validation des entrées :** Ne jamais utiliser de texte provenant d'utilisateurs non fiables comme signal d'autorisation pour des actions automatisées.
*   **Audit des workflows :** Vérifier que les automatisations ne peuvent pas être détournées via des configurations de hooks ou des capacités d'écriture excessives.

---
[Source](https://thehackernews.com/2026/08/google-deletes-3-adk-ai-workflows-after.html){:target="_blank"}
