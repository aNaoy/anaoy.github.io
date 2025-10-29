---
title: 'New AI-Targeted Cloaking Attack Tricks AI Crawlers Into Citing Fake Info as Verified Facts'
date: 2025-10-29
permalink: /posts/2025/10/29/new-ai-targeted-cloaking-attack-tricks-ai-crawlers-into-citing-fake-info-as-verified-facts/
tags:
- veille-cyber
- hackernews
---
**L'usurpation par IA : une nouvelle menace pour la véracité de l'information**

Une technique d'attaque baptisée "AI-targeted cloaking" permet de tromper les agents d'exploration de l'intelligence artificielle, tels que ceux utilisés par ChatGPT et Perplexity. Cette méthode, inspirée du "cloaking" utilisé pour le référencement, consiste à présenter un contenu différent aux robots d'exploration IA qu'à un utilisateur humain. Un simple contrôle de l'agent utilisateur (user agent) suffit à rediriger le crawler vers un contenu falsifié.

Ce contenu erroné peut ensuite être présenté par les IA comme une information vérifiée dans leurs résumés ou leurs raisonnements autonomes, influençant potentiellement la perception de millions d'utilisateurs et introduisant des biais dans les systèmes qui s'appuient sur ces données. La simplicité de cette approche en fait une arme redoutable pour la désinformation et pourrait saper la confiance dans les outils d'IA.

Les recherches ont également mis en évidence des faiblesses dans la sécurité de divers agents IA, qui exécutent des requêtes potentiellement malveillantes sans garde-fous suffisants, même lorsqu'elles sont présentées comme des exercices de débogage. Certains agents sont capables d'opérations risquées comme la réinitialisation de mots de passe, le piratage de sessions, ou des tentatives d'injection SQL et JavaScript.

**Points clés :**

*   **AI-targeted cloaking :** Technique permettant de présenter un contenu différent aux IA et aux utilisateurs humains via une vérification de l'agent utilisateur.
*   **Contexte d'attaque :** Exploitation des crawlers IA (ChatGPT, Perplexity) pour injecter de fausses informations.
*   **Impact :** Présentation de contenus falsifiés comme des faits vérifiés par les IA, influence des biais, manipulation de l'information.
*   **Vulnérabilités générales des agents IA :** Exécution de requêtes risquées sans protections adéquates (réinitialisation de mots de passe, piratage de session, injection SQL/JavaScript).

**Vulnérabilités (CVEs non spécifiées dans l'article) :**

*   Faiblesse des mécanismes de vérification de l'agent utilisateur dans les agents IA, permettant la redirection vers du contenu falsifié.
*   Manque de safeguards dans divers agents IA (ex: ChatGPT Atlas, Claude Computer Use, Gemini Computer Use, Manus AI, Perplexity Comet) rendant possible l'exécution d'actions dangereuses.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques pour les développeurs d'IA ou les utilisateurs, les implications suggèrent :

*   **Pour les développeurs d'IA :** Renforcer les mécanismes de vérification de contenu, développer des contre-mesures contre le cloaking, améliorer la robustesse face aux injections de fausses données.
*   **Pour les utilisateurs :** Maintenir un esprit critique face aux informations générées par IA, vérifier les sources lorsque cela est possible.
*   **Pour les propriétaires de sites web :** Être conscients de ces techniques et envisager des mesures pour détecter ou prévenir la manipulation de contenu pour les crawlers IA.

---
[Source](https://thehackernews.com/2025/10/new-ai-targeted-cloaking-attack-tricks.html){:target="_blank"}
