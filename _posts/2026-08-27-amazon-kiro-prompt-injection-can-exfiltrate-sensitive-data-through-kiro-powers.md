---
title: 'Amazon Kiro Prompt Injection Can Exfiltrate Sensitive Data Through Kiro Powers'
date: 2026-08-27
permalink: /posts/2026/08/27/amazon-kiro-prompt-injection-can-exfiltrate-sensitive-data-through-kiro-powers/
tags:
- veille-cyber
- hackernews
---
### Exfiltration de données via injection de prompt dans Amazon Kiro

Une vulnérabilité de sécurité a été identifiée dans l'IDE agentique Amazon Kiro, permettant à un attaquant d'exfiltrer des données sensibles à partir d'un espace de travail compromis. Cette faille repose sur une injection de prompt indirecte exploitant les « Kiro Powers », des outils qui permettent au modèle d'IA de lire des fichiers locaux et d'interagir avec des configurations système.

**Points clés :**
*   **Vecteur d'attaque :** Lorsqu'un utilisateur ouvre un espace de travail malveillant via un fichier de configuration, le contenu du dépôt est interprété par l'IA comme des instructions.
*   **Rupture de la limite de confiance :** L'agent IA est incité à lire des informations locales sensibles et à les écrire dans des configurations de l'IDE, provoquant ensuite une activité réseau vers un serveur externe sans consentement explicite.
*   **Faiblesse systémique :** Cette vulnérabilité illustre les risques croissants liés aux outils de développement basés sur l'IA, où les fichiers de projet influencent directement le comportement des agents et l'exécution d'outils locaux.

**Vulnérabilités :**
*   **Amazon Kiro IDE (Data Exfiltration) :** Pas de CVE identifié (corrigé en version 0.8.140).
*   **CVE-2026-10591 :** Précédente faille de contrôle d'accès dans Kiro permettant l'exécution arbitraire de commandes (RCE).

**Recommandations :**
*   **Mise à jour :** Assurez-vous d'utiliser la version 0.8.140 ou supérieure de l'IDE Amazon Kiro.
*   **Prudence avec les projets tiers :** Évitez d'ouvrir des espaces de travail provenant de sources non fiables, particulièrement via des fichiers de configuration suspects.
*   **Vigilance sur les agents IA :** Maintenez une surveillance stricte sur les permissions accordées aux agents (MCP, accès aux fichiers, accès réseau) et restez informé des risques d'injections de prompt indirectes inhérents aux outils de développement modernes.

---
[Source](https://thehackernews.com/2026/08/amazon-kiro-prompt-injection-can.html){:target="_blank"}
