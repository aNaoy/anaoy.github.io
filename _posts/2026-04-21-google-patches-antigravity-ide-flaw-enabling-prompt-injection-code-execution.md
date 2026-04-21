---
title: 'Google Patches Antigravity IDE Flaw Enabling Prompt Injection Code Execution'
date: 2026-04-21
permalink: /posts/2026/04/21/google-patches-antigravity-ide-flaw-enabling-prompt-injection-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans l'IDE Antigravity de Google

Une faille de sécurité dans l'environnement de développement (IDE) agentique **Antigravity** de Google, désormais corrigée, permettait à des attaquants d'exécuter du code arbitraire en contournant le "Strict Mode" de l'outil.

**Points clés :**
* **Mécanisme d'attaque :** La vulnérabilité reposait sur une mauvaise désinfection des entrées de l'outil `find_by_name`. Un attaquant pouvait injecter l'argument `-X` (exec-batch) via le paramètre de recherche, forçant l'outil à exécuter des fichiers comme des scripts shell.
* **Chaîne d'exploitation :** En combinant cette injection avec la capacité de l'IDE à créer des fichiers, un attaquant pouvait déposer un script malveillant puis le déclencher automatiquement via une simple recherche, sans interaction supplémentaire de l'utilisateur.
* **Vecteur indirect :** L'attaque pouvait être initiée par une injection de prompt indirecte, par exemple en incitant l'agent IA à traiter un fichier malveillant provenant d'une source non fiable.

**Vulnérabilité identifiée :**
* Une vulnérabilité connexe a également été répertoriée dans Microsoft Copilot Studio sous la référence **CVE-2026-21520** (Score CVSS : 7.5), illustrant une tendance plus large aux injections de prompts indirectes affectant les outils d'IA.

**Recommandations :**
* **Validation stricte des entrées :** Les développeurs d'outils basés sur l'IA doivent impérativement valider les entrées utilisateur avant de les passer à des outils d'exécution système, même au sein d'environnements "sandboxed".
* **Séparation des données :** Il est crucial d'assurer une séparation hermétique entre les instructions système de l'agent et les données fournies par les utilisateurs.
* **Méfiance envers l'autonomie des agents :** Les systèmes de sécurité ne doivent pas reposer sur la capacité de l'IA à distinguer une instruction légitime d'une instruction malveillante injectée dans des données externes, car les agents IA ont tendance à traiter ces données comme des commandes à exécuter.

---
[Source](https://thehackernews.com/2026/04/google-patches-antigravity-ide-flaw.html){:target="_blank"}
