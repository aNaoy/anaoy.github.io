---
title: 'Discovering Negative-Days with LLM Workflows'
date: 2026-02-07
permalink: /posts/2026/02/07/discovering-negative-days-with-llm-workflows/
tags:
- veille-cyber
- zerodaysfans
---
## Détection Précoce des Vulnérabilités Logiciels

L'utilisation croissante des modèles de langage (LLM) dans la découverte de vulnérabilités conduit à une accélération sans précédent du cycle de vie des failles de sécurité. Le délai entre la publication d'une faille (CVE) et son exploitation devient de plus en plus court, voire négatif, en particulier pour les projets open source dont les correctifs sont publiquement disponibles. Les processus actuels de divulgation des vulnérabilités peinent à suivre ce rythme, créant un risque accru pour les utilisateurs. Ce phénomène s'aggrave avec l'existence de "never-days", des vulnérabilités corrigées mais jamais officiellement cataloguées avec un identifiant CVE, laissant les utilisateurs inconscients du danger.

Pour contrer cette menace, une approche proactive de veille de sécurité est nécessaire, axée sur la surveillance continue des dépôts open source pour détecter les commits de correction de vulnérabilités avant même la publication d'un CVE.

### Points Clés

*   **Accélération des Exploits :** Les LLM permettent une découverte rapide de vulnérabilités, réduisant le temps d'exploitation à zéro, voire à un temps négatif.
*   **Risque pour l'Open Source :** Les correctifs publics des projets open source rendent les failles immédiatement exploitables.
*   **"Never-Days" :** Des vulnérabilités corrigées sans CVE assigné laissent les utilisateurs vulnérables sans le savoir.
*   **Workflow de Veille Proactive :** Il est crucial de surveiller les modifications de code pour identifier les correctifs de sécurité potentiels avant la divulgation officielle.
*   **Automatisation avec les LLM :** Les LLM peuvent être intégrés dans des workflows automatisés pour analyser les commits et identifier les patches de sécurité.

### Vulnérabilités

*   **React2Shell :** Un exemple concret où le commit de correction, le pull request et la publication du CVE se sont succédé très rapidement, permettant une alerte précoce de quelques heures via la surveillance de l'activité du dépôt GitHub.
*   **Vulnerability in `@next/codemod` (canary release) :** Détection d'une vulnérabilité potentielle de type "Command Injection" (CVE non spécifié, classée comme "Medium" par le système de détection) dans une version expérimentale de l'outil `@next/codemod`. La vulnérabilité résidait dans l'utilisation de `execSync` avec interpolation de chaîne pour les commandes Git, remplaçée dans le patch par `execa` utilisant un tableau d'arguments, prévenant ainsi l'interprétation par le shell.

### Recommandations

*   **Mise à Jour des Workflows de Veille :** Les équipes de sécurité doivent intégrer des capacités de "précognition" dans leurs flux de renseignement pour surveiller les vulnérabilités avant la publication des CVE.
*   **Amélioration des Processus de Divulgation :** Les projets open source devraient renforcer leurs processus de correction et de divulgation de sécurité. La possibilité de rendre les pull requests privées sur les dépôts publics pourrait aider à une divulgation coordonnée.
*   **Développement d'Outils :** Encourager le développement et l'utilisation d'outils automatisés, tels que des GitHub Actions, pour surveiller et alerter sur les correctifs de sécurité potentiels.
*   **Validation des Preuves de Concept :** Expérimenter avec des sous-agents pour automatiser la validation des preuves de concept des exploits détectés afin de compléter la boucle de détection et de réponse.

---
[Source](https://spaceraccoon.dev/discovering-negative-days-llm-workflows/){:target="_blank"}
