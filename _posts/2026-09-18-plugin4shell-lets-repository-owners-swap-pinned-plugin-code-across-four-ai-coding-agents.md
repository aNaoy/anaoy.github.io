---
title: 'Plugin4Shell Lets Repository Owners Swap Pinned Plugin Code Across Four AI Coding Agents'
date: 2026-09-18
permalink: /posts/2026/09/18/plugin4shell-lets-repository-owners-swap-pinned-plugin-code-across-four-ai-coding-agents/
tags:
- veille-cyber
- hackernews
---
### Plugin4Shell : Vulnérabilité d'injection dans les agents de codage IA

Une faille de sécurité, baptisée **Plugin4Shell**, affecte quatre agents de codage par IA (Claude Code, OpenAI Codex, GitHub Copilot et Google Gemini CLI). Elle permet à un attaquant contrôlant un dépôt de plugins de substituer un plugin légitime par une version malveillante, même si l'agent a "verrouillé" le plugin sur une version spécifique (hash de commit).

**Points clés :**
* **Mécanisme d'attaque :** L'agent installe le plugin en se fiant au hash, mais Git peut interpréter ce hash comme un nom de branche. Si l'hébergeur du code autorise des noms de branche similaires à des hashs (ex: Bitbucket ou serveurs Git privés), l'attaquant peut faire pointer ce "nom" vers du code arbitraire.
* **Impact :** Le code malveillant hérite des privilèges de l'utilisateur (accès aux fichiers, identifiants et systèmes connectés).
* **Auto-mise à jour :** Les agents disposant d'une fonction d'auto-mise à jour (par défaut sur Claude Code et Codex) sont particulièrement vulnérables, car ils peuvent remplacer un plugin déjà approuvé sans intervention de l'utilisateur.
* **Statut actuel :** Aucune CVE n'a été assignée à ce jour.

**Vulnérabilités :**
* Le problème provient d'une ambiguïté dans la gestion des références Git par les outils clients, qui privilégient parfois une branche nommée comme un hash au détriment du hash de commit réel.

**Recommandations :**
* **Mise à jour :** Appliquer immédiatement les correctifs pour Claude Code (v2.1.179) et OpenAI Codex (v0.146.0).
* **Prudence :** Pour GitHub Copilot (non corrigé) et Gemini CLI (abandonné), éviter d'installer des plugins provenant de sources autres que les dépôts officiels GitHub, car ces derniers bloquent les noms de branches ambigus.
* **Migration :** Pour les utilisateurs de Google Gemini CLI, il est fortement recommandé de migrer vers l'outil *Antigravity*, qui n'est pas exposé à cette faille.

---
[Source](https://thehackernews.com/2026/09/plugin4shell-lets-repository-owners.html){:target="_blank"}
