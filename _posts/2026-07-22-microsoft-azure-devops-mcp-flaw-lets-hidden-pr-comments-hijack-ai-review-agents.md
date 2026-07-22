---
title: 'Microsoft Azure DevOps MCP Flaw Lets Hidden PR Comments Hijack AI Review Agents'
date: 2026-07-22
permalink: /posts/2026/07/22/microsoft-azure-devops-mcp-flaw-lets-hidden-pr-comments-hijack-ai-review-agents/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité d'injection dans le serveur Azure DevOps MCP

Une faille de sécurité critique a été identifiée dans le serveur **Azure DevOps MCP** de Microsoft, permettant à des attaquants d'exploiter des agents IA pour accéder à des données confidentielles. En insérant des commentaires HTML invisibles dans la description d'une *pull request* (PR), un attaquant peut détourner l'agent de revue de code d'un utilisateur privilégié pour effectuer des actions non autorisées.

**Points clés :**
* **Mécanisme d'attaque :** L'agent IA traite le texte brut de la description d'une PR sans utiliser les protections nécessaires. Le code malveillant est invisible pour l'humain dans l'interface web, mais est interprété par l'agent comme des instructions système.
* **Impact :** L'agent, agissant avec les permissions de l'utilisateur (souvent supérieures à celles de l'attaquant), peut lire des dépôts privés, accéder à des secrets, déclencher des pipelines ou exfiltrer des données confidentielles vers un commentaire public.
* **Origine du problème :** Une incohérence dans le code où Microsoft a implémenté une protection ("spotlighting") sur certains outils du serveur, mais a omis de l'appliquer à la fonction `repo_get_pull_request_by_id`.
* **Vulnérabilité :** Aucune CVE n'a été attribuée à ce jour.

**Recommandations :**
* **Principe du moindre privilège :** Restreindre les jetons d'accès des agents IA strictement au projet en cours de revue.
* **Audit des permissions :** Limiter les capacités de l'agent (par exemple, désactiver l'accès aux wikis ou au lancement de pipelines) s'il n'en a pas besoin pour sa tâche principale.
* **Vigilance sur les traces :** Surveiller les historiques d'exécution des agents pour détecter des comportements anormaux, tels que des actions inter-projets.
* **Filtrage des outils :** Charger uniquement les domaines MCP nécessaires à la mission spécifique de l'agent.
* **Recherche de signes d'intrusion :** Scanner les descriptions de PR ouvertes à la recherche de commentaires HTML masqués (`<!-- ... -->`) et vérifier les journaux d'activité des agents pour détecter toute activité inhabituelle.

---
[Source](https://thehackernews.com/2026/07/microsoft-azure-devops-mcp-flaw-lets.html){:target="_blank"}
