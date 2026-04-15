---
title: 'Scanning for AI Models, (Tue, Apr 14th)'
date: 2026-04-15
permalink: /posts/2026/04/15/scanning-for-ai-models-tue-apr-14th/
tags:
- veille-cyber
- sans-isc
---
### Campagne de scan malveillant ciblant les modèles d'IA

Depuis le 10 mars 2026, une activité de scan automatisé cible activement les serveurs web à la recherche de fichiers de configuration et de secrets liés à des modèles d'IA (Claude, Hugging Face, OpenAI, OpenClaw). Cette campagne est attribuée à une adresse IP unique (81.168.83.103), qui effectue également des reconnaissances plus larges sur des ports web classiques depuis fin janvier 2026.

**Points clés :**
*   **Mode opératoire :** L'attaquant tente d'accéder à des chemins spécifiques exposés sur des serveurs web pour exfiltrer des fichiers sensibles.
*   **Cibles :** Les recherches portent sur des fichiers de configuration, des bases de données locales (`chroma.db`, `db.sqlite`) et des jetons d'authentification (`secrets.json`, `.cache/huggingface/token`).
*   **Infrastructure :** L'adresse IP source (81.168.83.103) appartient au système autonome AS 20860 et semble héberger un système Linux.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, mais la vulnérabilité réside dans l'exposition accidentelle de répertoires et de fichiers sensibles (mauvaise configuration du serveur web ou répertoire racine mal protégé) contenant des clés d'API ou des données d'entraînement.

**Recommandations :**
*   **Surveillance :** Surveiller les journaux d'accès (logs) pour détecter des requêtes ciblant les répertoires `.openclaw`, `.clawdbot`, `.claude`, `.cache/huggingface/` ou `/openai/`.
*   **Sécurisation :** S'assurer qu'aucun fichier de configuration, clé d'API ou jeton d'accès n'est accessible depuis la racine du répertoire web public.
*   **Restrictions :** Bloquer les connexions provenant de l'adresse IP `81.168.83.103` au niveau du pare-feu ou du WAF (Web Application Firewall).
*   **Audit :** Vérifier les droits d'accès sur les répertoires sensibles pour empêcher leur énumération par des robots d'indexation malveillants.

---
[Source](https://isc.sans.edu/diary/rss/32896){:target="_blank"}
