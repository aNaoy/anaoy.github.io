---
title: 'Claude Code: Data Exfiltration with DNS Requests'
date: 2025-08-11
permalink: /posts/2025/08/11/claude-code-data-exfiltration-with-dns-requests/
tags:
- veille-cyber
- zerodaysfans
---
## Fuite de Données via DNS : Exploitation de Claude Code

Une faille de sécurité critique dans Claude Code permettait à des attaquants de subtiliser des informations sensibles, telles que des clés d'API, à partir des machines des développeurs. Cette exfiltration de données était réalisée par le biais d'une injection de prompt indirecte.

**Fonctionnement de l'Exploitation :**

En manipulant le contenu d'un fichier analysé par Claude Code, un attaquant pouvait déclencher l'exécution de commandes Bash. Certaines de ces commandes, spécifiquement celles utilisées pour les requêtes DNS (comme `ping`, `nslookup`, `host`, `dig`), étaient autorisées à s'exécuter sans validation explicite de l'utilisateur. L'attaquant pouvait intégrer des données sensibles (extraites de fichiers comme `.env`) dans ces requêtes DNS, les redirigeant ainsi vers des serveurs contrôlés par l'attaquant, le tout à l'insu du développeur.

**Découverte :**

L'analyse du prompt système de Claude Code a révélé la présence d'outils comme `Read`, `Grep`, `LS` et `Bash`. Si les commandes `Bash` nécessitent normalement une approbation, la découverte d'une liste de commandes "allowlistées" exécutables sans consentement a été clé. L'attaquant a utilisé Claude lui-même pour identifier les commandes de cette liste pouvant être abusées à des fins d'exfiltration.

**Points Clés :**

*   **Type de vulnérabilité :** Injection de prompt indirecte combinée à une exfiltration de données via DNS.
*   **Impact :** Vol de données sensibles (clés d'API, variables d'environnement) sans consentement de l'utilisateur.
*   **Méthode d'exfiltration :** Intégration de données dans des requêtes DNS (subdomain, arguments de commande).
*   **Découverte assistée par IA :** Claude a été utilisé pour identifier les commandes bypassant les contrôles de sécurité.

**Vulnérabilités :**

*   **Absence de validation pour les commandes DNS :** Les commandes telles que `ping`, `nslookup`, `host`, `dig` étaient autorisées à s'exécuter sans confirmation utilisateur lorsque déclenchées par une injection de prompt indirecte.
*   Aucun identifiant CVE spécifique n'est mentionné dans l'article pour cette vulnérabilité.

**Recommandations :**

La proposition de mitigation suggère d'ajouter une validation humaine en retirant les commandes `ping`, `nslookup`, `dig` et `host` de la liste des commandes autorisées. L'article souligne également l'importance de maintenir la version la plus récente de Claude Code, la correction ayant été déployée rapidement par Anthropic.

---
[Source](https://embracethered.com/blog/posts/2025/claude-code-exfiltration-via-dns-requests/){:target="_blank"}
