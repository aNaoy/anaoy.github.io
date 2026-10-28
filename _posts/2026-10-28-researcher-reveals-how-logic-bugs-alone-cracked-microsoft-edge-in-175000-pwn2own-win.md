---
title: 'Researcher Reveals How Logic Bugs Alone Cracked Microsoft Edge in $175,000 Pwn2Own Win'
date: 2026-10-28
permalink: /posts/2026/10/28/researcher-reveals-how-logic-bugs-alone-cracked-microsoft-edge-in-175000-pwn2own-win/
tags:
- veille-cyber
- hackernews
---
### Analyse d'une chaîne d'exploitation par erreurs logiques sur Microsoft Edge

Le chercheur Orange Tsai (DEVCORE) a démontré lors du concours Pwn2Own 2026 une méthode permettant de prendre le contrôle d'un système Windows via Microsoft Edge sans utiliser de corruption de mémoire, mais en enchaînant uniquement des erreurs logiques. Cette chaîne d'exploitation, longue de moins de 100 lignes de code, permet de s'échapper du bac à sable (sandbox) du navigateur.

**Points clés :**
*   **Absence de corruption mémoire :** L'exploit repose sur des failles logiques dans la gestion des fonctionnalités d'Edge et de Windows.
*   **Universal Cross-Site Scripting (UXSS) :** L'attaque permet d'exécuter du JavaScript sur n'importe quel site web, contournant les politiques de sécurité (CSP).
*   **Évasion de bac à sable :** Le chercheur a abusé de la fonctionnalité « Immersive Reader » et d'une fonction interne de journalisation pour écrire des fichiers arbitraires sur le disque.
*   **Exécution de code :** L'attaquant parvient à exécuter du code en manipulant les gestionnaires de protocoles (telnet://) pour forcer le lancement d'un binaire malveillant déposé sur le système.
*   **Nature de l'exploit :** Il s'agit d'une recherche compétitive (Pwn2Own) ; aucune preuve d'exploitation active n'a été constatée.

**Vulnérabilités identifiées (CVE) :**
Microsoft a corrigé ces failles dès le 15 mai 2026. Les correctifs spécifiques incluent :
*   **CVE-2026-45492 :** Contournement de fonctionnalité de sécurité.
*   **CVE-2026-45494 :** Bug de usurpation d'identité (spoofing).
*   **CVE-2026-45495 :** (Correctif complémentaire lié à la chaîne d'exécution).

**Recommandations :**
*   **Mise à jour :** Les utilisateurs sont protégés dès lors qu'ils utilisent la version **148.0.3967.70** ou supérieure de Microsoft Edge. La mise à jour automatique est suffisante.
*   **Hygiène logicielle :** Bien que cette attaque soit complexe, elle souligne l'importance de maintenir le navigateur à jour pour éliminer les erreurs logiques exploitables au sein des fonctionnalités intégrées.

---
[Source](https://thehackernews.com/2026/10/researcher-reveals-how-logic-bugs-alone.html){:target="_blank"}
