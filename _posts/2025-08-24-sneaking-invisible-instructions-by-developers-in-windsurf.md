---
title: 'Sneaking Invisible Instructions by Developers in Windsurf'
date: 2025-08-24
permalink: /posts/2025/08/24/sneaking-invisible-instructions-by-developers-in-windsurf/
tags:
- veille-cyber
- zerodaysfans
---
### Instructions Cachées : Une Menace Invisible dans les Systèmes d'IA

Une faille de sécurité a été identifiée dans certains systèmes d'intelligence artificielle, dont Windsurf Cascade, permettant l'insertion d'instructions invisibles. Ces instructions, souvent sous forme de caractères Unicode non visibles, peuvent être interprétées par les modèles d'IA comme des commandes, déclenchant des actions non anticipées par les développeurs ou les utilisateurs.

**Points Clés :**

*   Certains modèles d'IA peuvent interpréter des caractères Unicode non visibles comme des instructions.
*   Cela peut mener à des injections de prompt cachées, où des commandes sont exécutées à l'insu de l'utilisateur.
*   Cette vulnérabilité permet potentiellement d'invoquer des outils de manière furtive.
*   L'invocation automatique d'outils, déclenchée par ces instructions cachées, peut entraîner des fuites d'informations, de données, et d'autres conséquences graves.
*   Bien que la sévérité soit jugée inférieure à celle de l'invocation directe d'outils, la nature indétectable des instructions cachées représente un risque significatif.
*   Des modèles comme Claude Sonnet 3.7 et le modèle SWE-1 de Windsurf sont capables de "voir" ces caractères, et certains sont capables de les interpréter comme instructions.

**Vulnérabilités Identifiées :**

*   **Instructions Invisibles via Caractères Unicode :** L'interprétation de caractères Unicode non visibles (tags) comme des instructions exécutables. Aucune CVE spécifique n'est mentionnée dans l'article pour cette vulnérabilité.

**Recommandations et Mitigations :**

*   **Rendre les Caractères Visibles :** Afficher ces caractères dans l'interface utilisateur pour informer clairement sur la présence d'informations cachées.
*   **Suppression des Caractères :** Retirer entièrement les caractères Unicode non visibles avant ou après l'inférence par le modèle. C'est une mesure pratique courante.
*   **Mise en Place au Niveau Applicatif :** Des agents comme Amp et Amazon Q Developer pour VS Code ont intégré des correctifs au niveau de l'application pour contrer cette menace.
*   **Modèles Robustes :** Les modèles d'OpenAI sont généralement protégés au niveau du modèle/API.
*   **Précautions pour les Développeurs :** Les créateurs d'applications basées sur des modèles vulnérables doivent prendre des mesures supplémentaires pour protéger les utilisateurs finaux, notamment en signalant la présence de texte invisible.

Windsurf a été notifié de cette faille, et après une période initiale de silence, l'entreprise a indiqué qu'elle travaillait sur des correctifs.

---
[Source](https://embracethered.com/blog/posts/2025/windsurf-sneaking-invisible-instructions-for-prompt-injection/){:target="_blank"}
