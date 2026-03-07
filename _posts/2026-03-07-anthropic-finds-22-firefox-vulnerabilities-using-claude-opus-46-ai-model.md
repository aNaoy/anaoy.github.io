---
title: 'Anthropic Finds 22 Firefox Vulnerabilities Using Claude Opus 4.6 AI Model'
date: 2026-03-07
permalink: /posts/2026/03/07/anthropic-finds-22-firefox-vulnerabilities-using-claude-opus-46-ai-model/
tags:
- veille-cyber
- hackernews
---
### L'IA au service de la découverte de vulnérabilités : le cas Firefox

Anthropic a collaboré avec Mozilla pour auditer le code source de Firefox à l'aide de son modèle d'IA Claude Opus 4.6. En deux semaines, l'IA a analysé près de 6 000 fichiers C++ et identifié 22 vulnérabilités inédites, confirmant l'efficacité de l'analyse assistée par IA pour renforcer la sécurité logicielle.

**Points clés :**
*   **Performance de détection :** L'IA a identifié 14 vulnérabilités critiques, 7 modérées et 1 faible, représentant près d'un cinquième des failles critiques corrigées par Mozilla en 2025.
*   **Capacité d'exploitation :** Bien que le modèle excelle dans la découverte de failles, sa capacité à créer des exploits automatisés reste limitée et nécessite des environnements de test sans mesures de protection (sandboxing).
*   **Complémentarité :** L'approche a permis de détecter des erreurs logiques complexes que les outils de *fuzzing* traditionnels ne parvenaient pas à isoler.

**Vulnérabilité identifiée :**
*   **CVE-2026-2796 :** Une erreur de compilation JIT (Just-In-Time) dans le composant JavaScript WebAssembly (score CVSS 9.8).

**Recommandations :**
*   **Mise à jour immédiate :** Les utilisateurs doivent impérativement installer **Firefox 148**, qui contient les correctifs pour les vulnérabilités identifiées.
*   **Utilisation des "Task Verifiers" :** Pour le développement, privilégier l'usage de vérificateurs de tâches lors de l'intégration de patches générés par IA afin de garantir la correction effective des failles sans compromettre la stabilité du code.
*   **Approche hybride :** Combiner l'analyse automatisée par IA avec une validation humaine pour éviter les faux positifs et garantir la robustesse des correctifs.

---
[Source](https://thehackernews.com/2026/03/anthropic-finds-22-firefox.html){:target="_blank"}
