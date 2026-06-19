---
title: 'AutoJack Attack Lets One Web Page Hijack AI Agent for Host Code Execution'
date: 2026-06-19
permalink: /posts/2026/06/19/autojack-attack-lets-one-web-page-hijack-ai-agent-for-host-code-execution/
tags:
- veille-cyber
- hackernews
---
### AutoJack : Vulnérabilité d'Exécution de Code à Distance via Agents IA

La recherche de Microsoft expose **AutoJack**, une chaîne d'exploitation permettant à un agent IA de navigation de transformer une simple page web malveillante en un vecteur d'exécution de code à distance (RCE) sur la machine hôte. Cette attaque cible spécifiquement le framework **AutoGen Studio**.

#### Points clés
*   **Mécanisme d'attaque :** L'agent IA navigue vers une URL contrôlée par un attaquant. Le JavaScript de cette page interagit avec un service local privilégié via WebSocket, permettant de lancer des processus arbitraires sur l'hôte sans authentification.
*   **Périmètre :** La faille concerne uniquement les versions pré-release (`0.4.3.dev1` et `0.4.3.dev2`) d'AutoGen Studio. La version stable (`0.4.2.2`) n'inclut pas le composant vulnérable.
*   **Contexte :** Cette vulnérabilité souligne la dangerosité croissante des services locaux "trop puissants" et l'inefficacité du "localhost" comme limite de confiance face aux agents autonomes.

#### Vulnérabilités identifiées
L'exploitation repose sur le chaînage de trois faiblesses critiques dans l'interface MCP (Model Context Protocol) :
1.  **Confiance excessive en localhost :** L'interface autorisait les connexions provenant de l'hôte lui-même, ignorant que le navigateur de l'agent est un vecteur d'injection.
2.  **Absence d'authentification :** Le middleware ignorait les chemins MCP, permettant des requêtes non authentifiées.
3.  **Exécution arbitraire :** L'endpoint acceptait et exécutait des commandes système directement à partir des paramètres de requête sans aucune liste blanche (allowlist).

*Note : Bien qu'aucune CVE ne soit explicitement associée à AutoJack dans cet article, des problématiques similaires dans des frameworks tiers ont été récemment documentées sous les identifiants **CVE-2026-26030** et **CVE-2026-25592**.*

#### Recommandations
*   **Mise à jour :** Pour les utilisateurs de versions pré-release, appliquer le correctif disponible sur le dépôt GitHub (commit `b047730`).
*   **Isolation :** Si l'utilisation d'AutoGen Studio est requise, il est impératif de compartimenter l'environnement via des conteneurs ou des machines virtuelles dédiées.
*   **Privilèges :** Exécuter le service sous un compte utilisateur aux droits restreints pour limiter l'impact en cas de compromission.
*   **Sécurisation structurelle :** Les développeurs de frameworks agents doivent impérativement implémenter une authentification forte sur le plan de contrôle, utiliser des listes blanches pour l'exécution de processus et isoler l'identité de l'agent de celle de l'utilisateur.

---
[Source](https://thehackernews.com/2026/06/autojack-attack-lets-one-web-page.html){:target="_blank"}
