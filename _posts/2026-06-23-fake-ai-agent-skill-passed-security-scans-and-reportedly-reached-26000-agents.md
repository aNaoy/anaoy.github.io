---
title: 'Fake AI Agent Skill Passed Security Scans and Reportedly Reached 26,000 Agents'
date: 2026-06-23
permalink: /posts/2026/06/23/fake-ai-agent-skill-passed-security-scans-and-reportedly-reached-26000-agents/
tags:
- veille-cyber
- hackernews
---
### La vulnérabilité critique des écosystèmes d'agents IA

La société de cybersécurité AIR a démontré la vulnérabilité des marketplaces d'agents IA en diffusant une extension malveillante ("skill") qui a réussi à infecter environ 26 000 agents. L'expérience prouve que les mécanismes de sécurité actuels, basés sur des scans statiques, sont inefficaces contre les charges utiles dynamiques.

**Points clés :**
*   **Contournement des défenses :** L'extension a été conçue pour passer les scans de sécurité en pointant initialement vers une documentation légitime. Une fois installée, l'attaquant a modifié le contenu de la page externe pour injecter une charge utile malveillante.
*   **Abus de confiance :** L'extension a utilisé des signaux trompeurs pour gagner en crédibilité (notamment en fusionnant une Pull Request dans un dépôt GitHub populaire pour hériter de sa réputation).
*   **Vulnérabilité structurelle :** Le problème réside dans le fait que les scanners analysent un "instantané" du code, alors que l'agent peut par la suite exécuter des instructions provenant de sources externes modifiables à tout moment.
*   **Risques :** Bien que l'expérience d'AIR se soit limitée à collecter des e-mails, une telle faille permet potentiellement l'exfiltration de données, l'accès aux systèmes internes ou l'exécution de code arbitraire avec les privilèges de l'agent.

**Vulnérabilités :**
Il n'existe pas de CVE spécifique, car il s'agit d'une **faille de conception systémique** (exploitation de liens externes dynamiques non surveillés par les scanners statiques).

**Recommandations :**
*   **Gestion des ressources externes :** Traiter les "skills" comme des logiciels à part entière. Auditer non seulement le code source fourni, mais aussi toutes les ressources et URLs externes auxquelles il accède.
*   **Principe du moindre privilège :** Restreindre strictement les accès accordés aux agents IA pour limiter l'impact d'une compromission.
*   **Contrôle centralisé :** Centraliser l'approbation des extensions au sein de l'entreprise et bannir l'utilisation de sources tierces non vérifiées.
*   **Surveillance continue :** Ne pas se contenter d'un scan lors de l'installation ; mettre en place une surveillance des changements sur les sources externes et utiliser le versionnage strict (pinning) pour éviter les mises à jour malveillantes silencieuses.

---
[Source](https://thehackernews.com/2026/06/fake-ai-agent-skill-passed-security.html){:target="_blank"}
