---
title: 'ThreatsDay: Android Spyware, PLC Attacks, AI Image Prompt Injection + 12 More Stories'
date: 2026-07-23
permalink: /posts/2026/07/23/threatsday-android-spyware-plc-attacks-ai-image-prompt-injection-12-more-stories/
tags:
- veille-cyber
- hackernews
---
# Panorama des menaces numériques : abus de confiance et vecteurs d'attaque

La semaine a été marquée par une recrudescence d'attaques exploitant la confiance des utilisateurs, dissimulant des charges malveillantes derrière des outils, des extensions ou des applications apparemment légitimes.

### Points clés
*   **Détournement de confiance :** La plupart des menaces récentes ne reposent pas sur des exploits complexes, mais sur l'abus de privilèges accordés à des outils banals (npm, extensions VS Code, applications mobiles).
*   **IA et automatisation :** L'intelligence artificielle est désormais doublement utilisée : comme vecteur d'attaque (injection de prompts dans des images pour corrompre des agents) et comme outil de défense (nouveaux modèles SLM pour la détection de vulnérabilités).
*   **Ciblage industriel :** Les infrastructures critiques (eau, énergie) sont sous pression avec des attaques persistantes sur les automates programmables industriels (PLC).

### Vulnérabilités et vecteurs d'attaque
*   **Chaîne d'approvisionnement logicielle :** Des paquets npm malveillants (`@copilot-mcp/apex`, `@apexfdn/apex`) installent des infostealers sur macOS.
*   **Extensions VS Code :** Des extensions contrefaites (ex: "Markdown All Pro") détournent les ressources des développeurs.
*   **Injection GhostCommit :** Utilisation d'images PNG contenant des instructions masquées pour voler des secrets dans les dépôts de code via des agents LLM.
*   **Malwares bancaires et espionnage :**
    *   **Lampion :** Campagne de phishing ciblant le Portugal.
    *   **SectopRAT :** Distribué via des publicités trompeuses sur des outils de bureau (ex: faux client Claude).
    *   **OctagonPanel / MarkiRAT :** Applications Android factices (alertes civiles, VPN) pour le vol de données sensibles.
*   **Adware "AfterCall" :** Applications Android exploitant les permissions d'accessibilité pour afficher des publicités intrusives après les appels.
*   **TrickBot :** Évolution vers l'utilisation du tunneling DNS pour masquer les communications avec les serveurs C2.

### Recommandations de sécurité
*   **Gestion des accès :** Restreindre strictement l'accès direct à Internet pour les automates industriels (PLC) et les systèmes OT.
*   **Code généré par IA :** Augmenter la vigilance sur le code produit par l'IA, souvent sujet à des problèmes de gestion des secrets, d'autorisations (IDOR) et de contrôle de débit (DoS).
*   **Mises à jour système :** Appliquer impérativement les correctifs GitHub Enterprise Server (GHES) avant le 18 août 2026.
*   **Hygiène de développement :** Privilégier la vérification des sources lors de l'installation de dépendances et limiter les permissions accordées aux extensions d'éditeurs de code.
*   **Approche Zero Trust :** Ne plus se fier à l'apparence des applications. Systématiquement se poser la question : "Que peut faire cet outil en cas de compromission ?" avant toute installation ou octroi de privilèges.

---
[Source](https://thehackernews.com/2026/07/threatsday-android-spyware-plc-attacks.html){:target="_blank"}
