---
title: 'Claude Code and Gemini CLI Flaws Let a GitHub Issue Reach CI Workflow Secrets'
date: 2026-08-07
permalink: /posts/2026/08/07/claude-code-and-gemini-cli-flaws-let-a-github-issue-reach-ci-workflow-secrets/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les agents de codage IA

Des failles de sécurité majeures ont été identifiées dans les outils d'IA utilisés pour le développement (Claude Code, Gemini CLI et OpenAI Codex), permettant à des attaquants externes de compromettre des environnements CI/CD via de simples issues GitHub.

**Points clés :**
*   **Problème structurel :** Les vulnérabilités résident dans le « harness » (la couche logicielle entre le modèle IA et le système), où des incohérences de validation autorisent l'exécution de commandes malveillantes.
*   **Impact :** Un utilisateur sans privilèges sur un dépôt peut exécuter du code sur les runners CI, exfiltrer des secrets ou détourner des flux de travail.
*   **Absence d'exploitation active :** Aucune preuve d'utilisation malveillante n'a été recensée à ce jour, bien que des laboratoires de reproduction publics existent.

**Vulnérabilités identifiées :**
*   **CVE-2026-12537 (Gemini CLI) :** Injection de commande OS dans le lanceur de conteneur, permettant une exécution de code sur l'hôte avant le démarrage du bac à sable (Score CVSS : 10.0).
*   **CVE-2026-54316 (Claude Code) :** Utilisation détournée d'un compteur de téléchargement public pour exfiltrer des clés API caractère par caractère.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à Gemini CLI v0.39.1, run-gemini-cli v0.1.22 et Claude Code v2.1.163.
*   **Audit de sécurité :** Examiner minutieusement tous les workflows CI déclenchables par des utilisateurs externes.
*   **Sécurisation des workflows :** Pour les outils comme OpenAI Codex, isoler les étapes de traitement dans des jobs séparés avec des permissions restreintes (sandbox en lecture seule, absence de droits `sudo`).
*   **Gestion des entrées :** Considérer systématiquement les fichiers d'instructions des dépôts et les inputs des utilisateurs comme des surfaces d'attaque non fiables.

---
[Source](https://thehackernews.com/2026/08/claude-code-and-gemini-cli-flaws-let.html){:target="_blank"}
