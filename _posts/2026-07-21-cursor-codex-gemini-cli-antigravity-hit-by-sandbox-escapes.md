---
title: 'Cursor, Codex, Gemini CLI, Antigravity hit by sandbox escapes'
date: 2026-07-21
permalink: /posts/2026/07/21/cursor-codex-gemini-cli-antigravity-hit-by-sandbox-escapes/
tags:
- veille-cyber
- bleepingcomp
---
### Évasion de bac à sable dans les agents de codage IA

Des chercheurs de Pillar Security ont démontré que des agents de codage IA populaires (Cursor, Codex, Gemini CLI et Antigravity) souffrent de vulnérabilités permettant de s'échapper de leur environnement sécurisé (sandbox). L'attaque ne cible pas directement la sandbox, mais exploite la confiance accordée par les outils hôtes aux fichiers générés par l'IA au sein de l'espace de travail.

**Points clés :**
* **Mécanisme d'attaque :** L'agent IA écrit des fichiers malveillants ou des configurations piégées dans l'espace de travail. Ces fichiers sont ensuite lus, exécutés ou interprétés par des outils extérieurs à la sandbox (extensions Python, Git, Docker, tâches VS Code), entraînant une exécution de code arbitraire sur la machine hôte.
* **Modes de défaillance :** Les vulnérabilités proviennent de listes de blocage inefficaces, de configurations d'espace de travail exécutables, de listes blanches de commandes trop permissives et de démons locaux privilégiés.
* **Réponse des éditeurs :** La plupart des failles ont été corrigées ou sont en cours de traitement. Google, toutefois, a minimisé certains risques, jugeant l'exploitation difficile sans ingénierie sociale préalable.

**Vulnérabilités identifiées :**
* **CVE-2026-48124 (Cursor) :** Exploitation d'une configuration de hook `.claude` pour une exécution de commande hors sandbox.
* **Diverses failles (Cursor/Codex/Gemini CLI) :** Abus des sockets Docker locaux et des métadonnées Git pour contourner les restrictions.

**Recommandations :**
* Ne pas se fier uniquement à l'existence d'une sandbox pour sécuriser les outils d'IA.
* Auditer le comportement des outils locaux qui interagissent avec les fichiers générés par l'IA.
* Surveiller les interactions entre les agents et les processus privilégiés (ex: démons, outils de build, extensions IDE).
* Mettre à jour systématiquement les agents de codage vers les dernières versions corrigées.

---
[Source](https://www.bleepingcomputer.com/news/security/cursor-codex-gemini-cli-antigravity-hit-by-sandbox-escapes/){:target="_blank"}
