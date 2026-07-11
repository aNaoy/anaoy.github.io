---
title: 'Ghostcommit hides prompt injection in images to fool AI agents, steal secrets'
date: 2026-07-11
permalink: /posts/2026/07/11/ghostcommit-hides-prompt-injection-in-images-to-fool-ai-agents-steal-secrets/
tags:
- veille-cyber
- bleepingcomp
---
### Ghostcommit : l'injection de prompt dissimulée dans les images

« Ghostcommit » est une technique d'attaque exploitant une faille structurelle dans les agents de codage IA et les outils de revue de code automatisés. En intégrant des instructions malveillantes sous forme de texte visible à l'intérieur d'une image (PNG), un attaquant peut forcer un agent IA à lire des fichiers sensibles (comme `.env`) et à exfiltrer les secrets en les encodant sous forme de liste d'entiers dans le code source, contournant ainsi les scanners de secrets classiques.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'un fichier de convention (`AGENTS.md`) qui pointe vers une image contenant des instructions d'exfiltration.
*   **Angle mort :** La majorité des outils de revue de code ignorent le contenu des fichiers binaires (images), permettant au payload de passer inaperçu lors de la revue humaine ou automatisée.
*   **Comportement de l'agent :** L'exfiltration se déclenche ultérieurement lorsqu'un développeur interagit avec l'agent, qui exécute alors les instructions contenues dans l'image.
*   **Facteur déterminant :** L'issue de l'attaque dépend davantage de la configuration de l'outil ("harness") entourant l'IA que du modèle de langage lui-même.

**Vulnérabilités :**
*   **Absence de revue multimodale :** Les outils actuels traitent les images comme des "boîtes noires" et ne vérifient pas leur contenu textuel.
*   **Excès de privilèges des agents :** Les agents de codage ont souvent accès aux fichiers de configuration sensibles sans garde-fous stricts.
*   **CVE :** Aucune CVE spécifique attribuée à ce jour, car il s'agit d'une faille conceptuelle de conception des pipelines de revue de code (design flaw).

**Recommandations :**
*   **Revues multimodales :** Implémenter des outils de défense capables d'analyser non seulement le code, mais aussi de lire et d'interpréter le contenu textuel des images intégrées aux dépôts.
*   **Analyse comportementale (Runtime) :** Surveiller les actions des agents de codage en temps réel ; tout accès inhabituel à des fichiers de secrets doit déclencher une alerte.
*   **Défense en profondeur :** Ne pas se reposer uniquement sur les scanners de secrets ; valider systématiquement les fichiers de configuration (`AGENTS.md`, etc.) et restreindre les capacités d'accès aux fichiers sensibles par les agents IA.

---
[Source](https://www.bleepingcomputer.com/news/security/ghostcommit-hides-prompt-injection-in-images-to-fool-ai-agents-steal-secrets/){:target="_blank"}
