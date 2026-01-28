---
title: 'Hackers hijack exposed LLM endpoints in Bizarre Bazaar operation'
date: 2026-01-28
permalink: /posts/2026/01/28/hackers-hijack-exposed-llm-endpoints-in-bizarre-bazaar-operation/
tags:
- veille-cyber
- bleepingcomp
---
**Opération Bizarre Bazaar : Exploitation Commerciale d'API d'IA Exposées**

Une campagne cybercriminelle, baptisée "Bizarre Bazaar", cible activement les points d'accès (endpoints) de grands modèles de langage (LLM) exposés sur Internet pour monétiser l'accès non autorisé à l'infrastructure d'intelligence artificielle. Les chercheurs ont observé plus de 35 000 sessions d'attaque sur leurs honeypots en 40 jours, révélant une opération d'envergure qui exploite des endpoints d'IA mal protégés ou faiblement authentifiés.

Les motivations principales de cette campagne incluent :

*   L'utilisation des ressources de calcul volées pour le minage de cryptomonnaies.
*   La revente d'accès API sur les marchés du darknet.
*   L'exfiltration de données contenues dans les invites et l'historique des conversations.
*   Des tentatives de mouvement latéral vers des systèmes internes via des serveurs de protocole de contexte de modèle (MCP).

Les vecteurs d'attaque courants exploitent des configurations erronées telles que des endpoints Ollama non authentifiés (port 11434), des API compatibles OpenAI non sécurisées (port 8000), des chatbots de production accessibles publiquement et des environnements de développement ou de staging avec des adresses IP publiques. Les attaques démarrent souvent peu après la détection de ces endpoints par des scanners Internet comme Shodan ou Censys.

**Vulnérabilités Exploités :**

Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, les vulnérabilités exploitées sont liées à :

*   **Absence d'authentification** sur les endpoints LLM et MCP.
*   **Exposition publique** d'endpoints de développement, de staging ou de production.
*   **Mauvaises configurations** de serveurs d'API d'IA.

**Recommandations :**

Pour se prémunir contre ce type d'attaques, il est essentiel de :

*   **Sécuriser les endpoints LLM et MCP** avec une authentification robuste.
*   **Restreindre l'accès public** aux environnements d'IA, en particulier aux endpoints de développement et de staging.
*   **Auditer régulièrement les configurations** des serveurs d'API d'IA pour détecter et corriger les failles de sécurité.
*   **Surveiller l'activité réseau** et les logs pour détecter les tentatives d'accès non autorisées.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hijack-exposed-llm-endpoints-in-bizarre-bazaar-operation/){:target="_blank"}
