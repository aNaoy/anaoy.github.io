---
title: 'AI coding agents hijacked using AGENTS.md file in Downloads folder'
date: 2026-10-25
permalink: /posts/2026/10/25/ai-coding-agents-hijacked-using-agentsmd-file-in-downloads-folder/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement d'agents IA via des fichiers d'instructions malveillants

Des chercheurs en cybersécurité ont identifié une vulnérabilité exploitant le fonctionnement normal des agents de codage IA (tels qu'OpenAI Codex ou Claude Code). En déposant un fichier d'instructions malveillant (ex: `AGENTS.md` ou `CLAUDE.md`) dans le dossier `~/Downloads` de l'utilisateur, un attaquant peut forcer l'agent à exécuter des commandes arbitraires, installer des paquets malveillants ou voler des jetons d'authentification (OAuth).

**Points clés :**
*   **Vecteur d'attaque :** Le dossier `~/Downloads` est la cible privilégiée, car les navigateurs peuvent y enregistrer des fichiers automatiquement.
*   **Exploitation :** Si un utilisateur lance un agent IA depuis ce dossier (une pratique courante), l'agent interprète automatiquement le fichier `AGENTS.md` comme des directives légitimes pour son projet.
*   **Impact :** Exécution de code local, installation de malwares (ex: `function-color`), exfiltration de jetons d'accès et usurpation d'identité de l'agent.
*   **Absence de faille logicielle :** Il ne s'agit pas d'un bug dans les modèles d'IA, mais d'une exploitation de leurs fonctionnalités natives.

**Vulnérabilités :**
*   Aucune CVE associée (comportement par conception des agents IA et des navigateurs).

**Recommandations :**
*   **Isolation du répertoire :** Ne jamais définir le dossier `~/Downloads` comme répertoire de travail pour un agent IA. Toujours lancer l'agent à la racine du projet spécifique sur lequel vous travaillez.
*   **Prudence avec les fichiers d'instructions :** Avant toute exécution, inspectez systématiquement le contenu des fichiers de configuration (`AGENTS.md`, `CLAUDE.md`, etc.) présents dans votre répertoire de travail.
*   **Environnement restreint :** Utilisez des bacs à sable (sandboxing) ou des conteneurs isolés pour tester les agents sur des codes ou des répertoires potentiellement non fiables.
*   **Sécurisation du navigateur :** Désactivez le téléchargement automatique de fichiers sans demande de confirmation dans les paramètres de votre navigateur.

---
[Source](https://www.bleepingcomputer.com/news/security/ai-coding-agents-hijacked-using-agentsmd-file-in-downloads-folder/){:target="_blank"}
