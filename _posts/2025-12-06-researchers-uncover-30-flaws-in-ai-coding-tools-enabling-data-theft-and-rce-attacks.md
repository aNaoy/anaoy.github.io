---
title: 'Researchers Uncover 30+ Flaws in AI Coding Tools Enabling Data Theft and RCE Attacks'
date: 2025-12-06
permalink: /posts/2025/12/06/researchers-uncover-30-flaws-in-ai-coding-tools-enabling-data-theft-and-rce-attacks/
tags:
- veille-cyber
- hackernews
---
### Les Outils de Développement Assistés par IA : Une Nouvelle Surface d'Attaque

Plus de 30 vulnérabilités, baptisées "IDEsaster", ont été découvertes dans divers environnements de développement intégrés (IDE) assistés par intelligence artificielle. Ces failles permettent, par le biais d'attaques par injection de prompt et l'exploitation des fonctionnalités légitimes des IDE, l'exfiltration de données et l'exécution de code à distance.

Les problèmes affectent des outils populaires tels que Cursor, Windsurf, Kiro.dev, GitHub Copilot, Zed.dev, Roo Code, Junie et Cline. Vingt-quatre de ces vulnérabilités ont reçu des identifiants CVE. La particularité de ces attaques réside dans le fait que les agents IA ignorent souvent le logiciel hôte (l'IDE) dans leur modèle de menace, considérant leurs propres fonctionnalités comme intrinsèquement sûres. L'ajout d'agents IA autonomes peut transformer ces fonctionnalités en vecteurs d'exfiltration et d'exécution de code.

Les vecteurs d'attaque combinés incluent :
*   La contournement des protections des modèles de langage (LLM) pour détourner le contexte.
*   L'exécution d'actions sans interaction utilisateur via des appels d'outils auto-approuvés par l'agent IA.
*   L'activation de fonctionnalités légitimes de l'IDE pour échapper aux limites de sécurité et voler des données ou exécuter des commandes.

**Points clés :**

*   Une trentaine de vulnérabilités découvertes dans des IDE assistés par IA.
*   Ces vulnérabilités permettent l'exfiltration de données et l'exécution de code à distance (RCE).
*   Les attaques exploitent l'injection de prompt et les fonctionnalités légitimes des IDE.
*   De nombreux outils populaires sont concernés.
*   Les agents IA peuvent transformer des fonctionnalités existantes en vecteurs d'attaque.

**Vulnérabilités identifiées (avec CVE si disponibles) :**

*   **Fuite de données via des fichiers de configuration JSON :**
    *   CVE-2025-49150 (Cursor)
    *   CVE-2025-53097 (Roo Code)
    *   CVE-2025-58335 (JetBrains Junie)
    *   GitHub Copilot (pas de CVE)
    *   Kiro.dev (pas de CVE)
    *   Claude Code (signalé par un avertissement de sécurité)
*   **Exécution de code via la modification des paramètres de l'IDE :**
    *   CVE-2025-53773 (GitHub Copilot)
    *   CVE-2025-54130 (Cursor)
    *   CVE-2025-53536 (Roo Code)
    *   CVE-2025-55012 (Zed.dev)
    *   Claude Code (signalé par un avertissement de sécurité)
*   **Exécution de code via la modification de configurations d'espaces de travail multi-racines :**
    *   CVE-2025-64660 (GitHub Copilot)
    *   CVE-2025-61590 (Cursor)
    *   CVE-2025-58372 (Roo Code)

Il est à noter que certains de ces scénarios reposent sur l'approbation automatique des écritures de fichiers par l'agent IA, permettant une exécution de code arbitraire sans interaction utilisateur.

D'autres vulnérabilités découvertes dans des outils liés à l'IA incluent :
*   Une faille d'injection de commande dans OpenAI Codex CLI (CVE-2025-61260).
*   Une injection de prompt indirecte dans Google Antigravity pour l'exfiltration d'identifiants et de code.
*   Plusieurs vulnérabilités dans Google Antigravity menant à l'exfiltration de données et à l'exécution de commandes à distance, y compris des backdoors persistantes.
*   Une nouvelle classe de vulnérabilité nommée PromptPwnd ciblant les agents IA connectés à des GitHub Actions vulnérables.

**Recommandations :**

*   **Pour les développeurs :** Utiliser les IDE et agents IA uniquement avec des projets et fichiers de confiance. Ne se connecter qu'à des serveurs MCP de confiance et surveiller les changements. Examiner et comprendre le flux de données des outils MCP. Examiner manuellement les sources ajoutées (URL, etc.) pour y trouver des instructions cachées.
*   **Pour les développeurs d'IA :** Appliquer le principe du moindre privilège aux outils LLM, minimiser les vecteurs d'injection de prompt, renforcer le prompt système, utiliser l'isolation (sandboxing) pour exécuter des commandes, et effectuer des tests de sécurité contre le traversée de répertoire, la fuite d'informations et l'injection de commande.

---
[Source](https://thehackernews.com/2025/12/researchers-uncover-30-flaws-in-ai.html){:target="_blank"}
