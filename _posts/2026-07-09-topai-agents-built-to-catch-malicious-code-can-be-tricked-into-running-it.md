---
title: 'Top AI Agents Built to Catch Malicious Code Can Be Tricked Into Running It'
date: 2026-07-09
permalink: /posts/2026/07/09/topai-agents-built-to-catch-malicious-code-can-be-tricked-into-running-it/
tags:
- veille-cyber
- hackernews
---
### "Friendly Fire" : Quand les agents IA d'analyse de code deviennent des vecteurs d'attaque

Des chercheurs ont démontré une faille de sécurité baptisée **"Friendly Fire"**, qui permet à des attaquants de compromettre des machines via des agents IA de codage (type Anthropic Claude Code ou OpenAI Codex). L'attaque détourne le processus de vérification de sécurité : l'agent, en mode autonome, exécute un binaire malveillant présent dans un dépôt tiers sur simple instruction d'un fichier README, sans alerter l'utilisateur.

**Points clés :**
* **Détournement d'usage :** Les agents sont trompés par des scripts de "test de sécurité" factices cachés dans des fichiers README, qu'ils considèrent comme légitimes pour accomplir leur tâche.
* **Invisibilité :** Le code malveillant est masqué par des métadonnées provenant de fichiers sains, ce qui permet de contourner les analyses de désassemblage des IA.
* **Problème de conception :** La vulnérabilité ne réside pas dans une version logicielle spécifique, mais dans l'incapacité fondamentale des modèles actuels à distinguer le code à analyser des instructions qu'ils doivent exécuter.
* **Auto-exécution :** Le danger est maximal lorsque l'agent est configuré en mode "auto-review" ou "auto-mode", lui permettant de lancer des commandes sans validation humaine systématique.

**Vulnérabilités :**
* Aucune CVE unique n'est associée, car il s'agit d'une faiblesse systémique de conception.
* Mention de **CVE-2026-39861** concernant les précédentes failles d'évasion de bac à sable (sandbox) au sein de Claude Code, soulignant l'insuffisance des mécanismes d'isolation actuels.

**Recommandations :**
* **Ne pas automatiser l'analyse de code non fiable :** Éviter de confier l'analyse de dépôts tiers à des agents IA ayant des permissions d'exécution sur votre machine ou accès à vos secrets.
* **Privilégier la validation manuelle :** Désactiver les modes entièrement autonomes ("auto-mode") pour exiger une confirmation humaine avant chaque exécution de commande.
* **Surveillance proactive :** Être vigilant si un agent tente d'exécuter un binaire ou un script recommandé uniquement par un fichier de documentation (README/docs).
* **Isolation renforcée :** Bien que les environnements de type bac à sable (sandbox) puissent réduire les risques, ils ne constituent pas une protection absolue contre les évasions.

---
[Source](https://thehackernews.com/2026/07/friendly-fire-ai-agents-built-to-catch.html){:target="_blank"}
