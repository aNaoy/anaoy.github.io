---
title: 'Malicious .git Configs Can Make Claude, Codex, Cursor, and Other AI Agents Run Attacker Code'
date: 2026-09-02
permalink: /posts/2026/09/02/malicious-git-configs-can-make-claude-codex-cursor-and-other-ai-agents-run-attacker-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans les agents de codage IA via Git

Des chercheurs de Manifold Security ont identifié une faille de sécurité majeure affectant sept agents de codage en ligne de commande (dont Claude Code, Cursor, Codex, etc.). La vulnérabilité permet l'exécution de code arbitraire sur la machine de l'utilisateur sans aucune interaction ou approbation préalable, simplement en ouvrant un dépôt Git malveillant.

**Points clés :**
*   **Mécanisme d'attaque :** L'attaque détourne la configuration `core.fsmonitor` de Git. Cette option permet de définir une commande exécutée automatiquement par Git pour identifier les modifications de fichiers.
*   **Contournement de sécurité :** L'exécution du code malveillant a lieu avant que les mécanismes de "confiance du répertoire" ou les sandboxes des agents ne soient activés.
*   **Condition d'exploitation :** Le dépôt doit être reçu avec son dossier `.git` intact (ex: via archive, clé USB ou partage de fichiers), contrairement à un `git clone` classique qui est immunisé.
*   **Impact :** Accès total aux privilèges de l'utilisateur sur sa machine (lecture, modification ou suppression de fichiers).

**Vulnérabilités identifiées (CVE) :**
*   **CVE-2026-19592** (OpenAI Codex)
*   **CVE-2026-72718** (goose)
*   **CVE-2026-71963** (Hermes Agent)
*   **CVE-2026-55607** (Claude Code)
*   *Note : Des vulnérabilités historiques similaires incluent CVE-2021-43891 (VS Code) et CVE-2022-24346 (JetBrains).*

**Statut des correctifs :**
*   **Correctifs disponibles :** goose, Codex (Desktop et CLI), et certaines versions de Claude Code.
*   **Non corrigés (à la date de publication) :** Hermes Agent, Qwen Code, Grok Build, ainsi qu'un vecteur d'attaque secondaire dans Claude Code.

**Recommandations :**
1.  **Désactivation globale :** Exécutez `git config --global core.fsmonitor false` pour désactiver cette fonctionnalité par défaut sur votre machine.
2.  **Audit manuel :** Avant d'ouvrir un dépôt inconnu avec un agent, inspectez le fichier `.git/config` à la recherche de clés suspectes (`core.fsmonitor`, `core.hooksPath`, `attr.tree`).
3.  **Vérification :** Utilisez la commande `git config --get core.fsmonitor` à l'intérieur d'un répertoire suspect pour vérifier s'il tente d'exécuter une commande externe.
4.  **Mise à jour :** Mettez immédiatement à jour vos outils de développement vers les versions les plus récentes.

---
[Source](https://thehackernews.com/2026/09/malicious-git-configs-can-make-claude.html){:target="_blank"}
