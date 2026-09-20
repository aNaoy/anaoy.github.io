---
title: 'Researchers escape OpenAI Codex sandbox to run commands on host'
date: 2026-09-20
permalink: /posts/2026/09/20/researchers-escape-openai-codex-sandbox-to-run-commands-on-host/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans la sandbox d'OpenAI Codex

Des chercheurs en sécurité ont identifié deux méthodes permettant de s'échapper de la sandbox d'OpenAI Codex, l'agent de codage d'OpenAI. Ces failles permettaient l'exécution de commandes non autorisées sur la machine hôte d'un développeur, même dans le mode de sécurité le plus strict.

**Points clés :**
* **Heapjack :** En ouvrant un dépôt de code tiers et en interagissant avec l'IA, un attaquant peut extraire un jeton d'authentification situé en mémoire partagée. Ce jeton permet ensuite d'envoyer des requêtes malveillantes au processus parent, outrepassant totalement la sandbox.
* **Overpatch :** Une vulnérabilité dans l'outil `apply_patch` du CLI permettait de manipuler les permissions d'écriture. En utilisant un chemin spécifique (ex: `/tmp`), l'attaquant pouvait corrompre des fichiers système (comme `.zshrc`) pour exécuter du code lors de l'ouverture d'un terminal.
* **Cause racine :** Dans les deux cas, le mécanisme de sécurité reposait sur une logique interne à l'environnement sandboxé, permettant à l'attaquant de tromper le système de vérification des droits.
* **Aucune CVE assignée :** Bien que critiques, ces vulnérabilités ont été traitées directement par OpenAI dans le cadre de leur programme de sécurité sans publication de CVE spécifique au moment du rapport.

**Recommandations :**
* **Mise à jour immédiate :** Les utilisateurs doivent impérativement mettre à jour **OpenAI Codex Desktop vers la version 26.818.21641** ou ultérieure, et **Codex CLI vers la version 0.149.0** ou ultérieure.
* **Vigilance sur les agents IA :** Ces failles illustrent les limites de l'isolation mémoire dans les environnements de développement basés sur V8. Il est conseillé d'isoler l'exécution des outils d'IA dans des conteneurs ou des machines virtuelles dédiés pour limiter l'impact en cas d'échappée.

---
[Source](https://www.bleepingcomputer.com/news/security/researchers-escape-openai-codex-sandbox-to-run-commands-on-host/){:target="_blank"}
