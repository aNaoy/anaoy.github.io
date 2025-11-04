---
title: 'Microsoft Detects "SesameOp" Backdoor Using OpenAIs API as a Stealth Command Channel'
date: 2025-11-04
permalink: /posts/2025/11/04/microsoft-detects-sesameop-backdoor-using-openais-api-as-a-stealth-command-channel/
tags:
- veille-cyber
- hackernews
---
## SesameOp : Une Porte Dérobée Exploitant l'API OpenAI

Une nouvelle menace, baptisée SesameOp, a été découverte par Microsoft. Ce logiciel malveillant utilise l'API Assistants d'OpenAI comme canal de communication discret pour ses opérations de commande et de contrôle (C2). Détecté en juillet 2025, ce programme a permis à des acteurs de la menace de maintenir une présence persistante dans des environnements ciblés pendant plusieurs mois.

L'infection s'appuie sur un chargeur ("Netapi64.dll") et une porte dérobée basée sur .NET ("OpenAIAgent.Netapi64"). Ce dernier récupère des commandes chiffrées via l'API OpenAI, les déchiffre puis les exécute localement. Les résultats sont ensuite renvoyés à OpenAI sous forme de message. Le code est fortement obfusqué par Eazfuscator.NET pour garantir sa discrétion et sa persistance. La communication avec l'API d'OpenAI se manifeste par trois types de valeurs dans le champ de description : "SLEEP" pour une pause, "Payload" pour exécuter une instruction, et "Result" pour signaler la disponibilité des résultats.

Ce mécanisme d'injection, connu sous le nom d'injection AppDomainManager, utilise des utilitaires Microsoft Visual Studio compromis par des bibliothèques malveillantes.

Microsoft a partagé ses découvertes avec OpenAI, qui a identifié et désactivé une clé API ainsi qu'un compte associé potentiellement utilisés par l'attaquant. L'API Assistants d'OpenAI est prévue pour être dépréciée en août 2026. L'origine exacte de ce logiciel malveillant reste inconnue, mais son développement démontre l'abus continu d'outils légitimes à des fins malveillantes pour échapper à la détection.

**Points clés :**

*   Découverte d'une porte dérobée nommée "SesameOp".
*   Utilisation de l'API Assistants d'OpenAI comme canal de commande et de contrôle (C2).
*   Technique d'injection AppDomainManager impliquant des utilitaires Visual Studio compromis.
*   Le logiciel malveillant est conçu pour la discrétion, la persistance et la communication sécurisée.
*   Trois types de commandes gérées via l'API OpenAI : SLEEP, Payload, Result.
*   Microsoft a partagé ses informations avec OpenAI, entraînant la désactivation d'une clé API.
*   L'API Assistants d'OpenAI sera dépréciée en août 2026.

**Vulnérabilités :**

L'article ne détaille pas de CVE spécifiques. L'exploitation réside dans l'abus d'une API légitime (OpenAI Assistants API) et dans la technique d'injection AppDomainManager.

**Recommandations :**

*   Rester vigilant face à l'utilisation d'outils légitimes par des acteurs malveillants.
*   Maintenir une surveillance active des activités réseau pour détecter des comportements anormaux.
*   Les organisations utilisant l'API Assistants d'OpenAI devraient examiner leur utilisation et surveiller les clés API pour toute activité suspecte.
*   La mise à jour et la sécurisation des environnements de développement et des utilitaires (comme Visual Studio) sont cruciales.

---
[Source](https://thehackernews.com/2025/11/microsoft-detects-sesameop-backdoor.html){:target="_blank"}
