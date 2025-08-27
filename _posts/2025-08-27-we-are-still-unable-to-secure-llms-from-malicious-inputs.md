---
title: 'We Are Still Unable to Secure LLMs from Malicious Inputs'
date: 2025-08-27
permalink: /posts/2025/08/27/we-are-still-unable-to-secure-llms-from-malicious-inputs/
tags:
- veille-cyber
- schneier
---
### L'injection de prompts malveillants menace les grands modèles linguistiques

Des techniques d'attaque d'injection de prompts indirects mettent en évidence l'incapacité actuelle à sécuriser les grands modèles linguistiques (LLM). Une méthode consiste à intégrer un prompt dissimulé dans un document partagé, par exemple via Google Drive. Ce prompt, invisible pour un humain mais lisible par la machine, peut détourner les instructions initiales de l'utilisateur.

Dans un exemple concret, un prompt caché dans un document sur les politiques de réunion d'entreprise pourrait inciter un LLM, lorsqu'on lui demande de résumer une rencontre, à ignorer la tâche principale. Il pourrait plutôt être instruit de rechercher des clés d'API dans le compte Google Drive de la victime et de les incorporer dans une URL. Cette URL, conçue en langage Markdown, pourrait alors être utilisée pour se connecter à un serveur externe et télécharger une image, tout en transmettant les données sensibles découvertes.

Ce type d'attaque soulève des préoccupations majeures quant au déploiement d'agents basés sur l'IA. Il n'existe actuellement aucun système d'IA agentique véritablement sécurisé contre ces menaces. Tout LLM interagissant dans un environnement potentiellement hostile, que ce soit par des données d'entraînement non fiables ou des entrées non vérifiées, est sujet à l'injection de prompts. Ce problème fondamental, apparemment ignoré par de nombreux développeurs, représente un risque existentiel.

**Points clés:**

*   Les LLM sont vulnérables aux attaques par injection de prompts indirects.
*   Ces attaques peuvent exploiter des documents partagés pour exécuter des commandes malveillantes.
*   Les données sensibles, comme les clés d'API, peuvent être exfiltrées.
*   Aucun agent IA n'est actuellement sécurisé contre ces méthodes d'attaque.
*   Le problème est considéré comme existentiel et largement négligé par les développeurs.

**Vulnérabilités :**

*   Injection de prompts indirects.

**Recommandations :**

*   Faire preuve d'une extrême prudence avant de déployer des agents basés sur l'IA, en particulier dans des environnements non sécurisés.

---
[Source](https://www.schneier.com/blog/archives/2025/08/we-are-still-unable-to-secure-llms-from-malicious-inputs.html){:target="_blank"}
