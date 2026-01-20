---
title: 'Three Flaws in Anthropic MCP Git Server Enable File Access and Code Execution'
date: 2026-01-20
permalink: /posts/2026/01/20/three-flaws-in-anthropic-mcp-git-server-enable-file-access-and-code-execution/
tags:
- veille-cyber
- hackernews
---
### Failles critiques dans le serveur Git d'Anthropic : accès aux fichiers et exécution de code

Trois vulnérabilités ont été découvertes dans le serveur Git du Model Context Protocol (MCP) officiel maintenu par Anthropic. Ces failles permettent potentiellement la lecture ou la suppression de fichiers arbitraires et l'exécution de code à distance, notamment par le biais de techniques d'injection de prompt.

Ces problèmes exploitent des faiblesses dans la manière dont le serveur traite les entrées utilisateur, permettant à un attaquant d'influencer le contenu lu par un assistant IA pour déclencher ces vulnérabilités sans accès direct au système de la victime.

**Points Clés :**

*   Le serveur `mcp-server-git` est utilisé pour interagir avec les dépôts Git via des modèles de langage.
*   Les vulnérabilités peuvent être chaînées avec d'autres composants MCP pour parvenir à l'exécution de code à distance.
*   L'exploitation réussie peut permettre de transformer n'importe quel répertoire en dépôt Git, d'écraser des fichiers et d'accéder à n'importe quel dépôt sur le serveur.

**Vulnérabilités Identifiées :**

*   **CVE-2025-68143 (CVSS 8.8/6.5)** : Vulnérabilité de traversée de répertoire due à l'acceptation de chemins de fichiers arbitraires par l'outil `git_init` lors de la création d'un dépôt, sans validation adéquate.
*   **CVE-2025-68144 (CVSS 8.1/6.4)** : Vulnérabilité d'injection d'arguments où les fonctions `git_diff` et `git_checkout` passent des arguments contrôlés par l'utilisateur directement aux commandes CLI de Git sans assainissement.
*   **CVE-2025-68145 (CVSS 7.1/6.3)** : Vulnérabilité de traversée de répertoire liée à l'absence de validation de chemin lors de l'utilisation de l'option `--repository` pour limiter les opérations à un chemin spécifique.

**Recommandations :**

*   Mettre à jour vers la version **2025.9.25** ou supérieure pour corriger la première vulnérabilité.
*   Mettre à jour vers la version **2025.12.18** ou supérieure pour corriger les deux autres vulnérabilités.
*   L'outil `git_init` a été supprimé du package dans les versions corrigées et une validation supplémentaire a été ajoutée pour prévenir les traversées de répertoire.

---
[Source](https://thehackernews.com/2026/01/three-flaws-in-anthropic-mcp-git-server.html){:target="_blank"}
