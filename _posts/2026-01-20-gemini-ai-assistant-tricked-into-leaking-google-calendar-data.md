---
title: 'Gemini AI assistant tricked into leaking Google Calendar data'
date: 2026-01-20
permalink: /posts/2026/01/20/gemini-ai-assistant-tricked-into-leaking-google-calendar-data/
tags:
- veille-cyber
- bleepingcomp
---
## Manipulation de Gemini via des Invitations de Calendrier

Des chercheurs ont découvert une méthode pour exploiter le modèle d'IA Gemini de Google, intégré à des services comme Google Calendar, en utilisant des invitations d'événement malveillantes. Ces invitations contiennent des descriptions conçues pour tromper Gemini grâce à des techniques d'injection de prompt en langage naturel.

Lorsqu'un utilisateur interroge Gemini sur son emploi du temps, l'assistant traite automatiquement les événements, y compris ceux contenant la charge utile malveillante. Gemini peut ainsi être amené à exécuter des instructions cachées, telles que la résumé de réunions privées et leur insertion dans la description d'un nouvel événement. Cette description mise à jour peut alors être visible par d'autres participants à l'événement, exposant des informations sensibles à l'attaquant.

Cette attaque tire parti du fait que Gemini interprète les données des événements pour fournir une assistance, ce qui permet à un attaquant d'insérer des instructions exécutables dans les champs de ces événements. Bien que Google ait mis en place des protections, cette méthode contourne les défenses existantes en présentant les instructions comme étant apparemment inoffensives.

**Points Clés :**

*   **Vulnérabilité :** Injection de prompt via des descriptions d'événements dans Google Calendar.
*   **Mécanisme :** Exploitation de la capacité de Gemini à interpréter le langage naturel pour exécuter des commandes cachées.
*   **Exfiltration de données :** Les informations privées des réunions sont révélées dans les descriptions d'événements modifiés.
*   **Impact :** Potentiel de fuite de données sensibles dans les environnements professionnels.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de CVE spécifiques pour cette nouvelle méthode, il se base sur le principe général d'injection de prompt qui affecte les grands modèles de langage. La vulnérabilité réside dans la manière dont Gemini traite les entrées contextuelles pour exécuter des actions, permettant l'exécution de commandes non désirées.

**Recommandations :**

*   **Pour les utilisateurs :** Être vigilant quant aux invitations de calendrier provenant de sources inconnues ou contenant des descriptions inhabituelles.
*   **Pour les développeurs d'IA (comme Google) :** Développer des défenses contextuelles plus avancées, allant au-delà de la simple détection syntaxique des prompts malveillants. Il est nécessaire d'anticiper de nouveaux modèles d'exploitation et de manipulation des systèmes d'IA.
*   **Évolution de la sécurité des applications :** Passer de la détection syntaxique à des approches de défense conscientes du contexte pour sécuriser les API pilotées par le langage naturel.

---
[Source](https://www.bleepingcomputer.com/news/security/gemini-ai-assistant-tricked-into-leaking-google-calendar-data/){:target="_blank"}
