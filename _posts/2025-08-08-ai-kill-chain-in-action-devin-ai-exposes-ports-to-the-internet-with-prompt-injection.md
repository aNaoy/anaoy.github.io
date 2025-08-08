---
title: 'AI Kill Chain in Action: Devin AI Exposes Ports to the Internet with Prompt Injection'
date: 2025-08-08
permalink: /posts/2025/08/08/ai-kill-chain-in-action-devin-ai-exposes-ports-to-the-internet-with-prompt-injection/
tags:
- veille-cyber
- zerodaysfans
---
### Exploitation de la fonction d'exposition de port de Devin par injection de prompt

Une vulnérabilité critique a été identifiée dans l'agent IA Devin, permettant à des attaquants d'exposer des ports locaux sur Internet via une injection de prompt. Cette fonctionnalité, initialement conçue pour le développement et les tests, peut être détournée pour divulguer des fichiers sensibles ou créer des portes dérobées.

**Points Clés :**

*   Devin possède un outil `expose_port` qui rend un port local accessible publiquement via une URL `.devinapps.com`.
*   Cette fonctionnalité peut être déclenchée sans intervention humaine.
*   Une chaîne d'attaque typique de l'IA (Injection de Prompt, Confused Deputy, Invocation Automatique d'Outil) peut être exploitée.

**Vulnérabilités :**

*   **Exposition de port non sécurisée :** La capacité de Devin à rendre des ports locaux accessibles sans validation humaine crée un risque significatif. Aucune preuve d'autres mesures d'atténuation (pare-feu IP) n'a été observée.
*   **Injection de Prompt Indirecte :** Des sites web malveillants peuvent inciter Devin à exécuter des actions dangereuses en lui faisant visiter le site.

**Scénario d'Attaque (Preuve de Concept) :**

1.  **Phase 1 :** Un attaquant crée un site web malveillant contenant une instruction d'injection de prompt. Cette instruction incite Devin à lancer un serveur web Python exposant le système de fichiers sur le port 8000 et à rediriger vers une autre page.
2.  **Phase 2 :** La deuxième page contient une autre instruction d'injection de prompt. Elle utilise une vulnérabilité (potentiellement liée à l'image markdown mentionnée dans l'article) pour "fuiter" l'URL publique générée par `expose_port` vers un serveur contrôlé par l'attaquant.
3.  **Accès :** L'attaquant peut alors accéder aux fichiers exposés sur Internet via l'URL divulguée.

**Recommandations :**

*   Les actions sensibles, comme l'exposition de ports, ne devraient pas dépendre uniquement du comportement du modèle ou de confirmations par prompt.
*   Une étape de validation hors bande devrait être mise en place pour permettre à l'utilisateur d'approuver ces opérations critiques.
*   Une divulgation responsable a été effectuée, mais des réponses sur les correctifs sont toujours attendues.

---
[Source](https://embracethered.com/blog/posts/2025/devin-ai-kill-chain-exposing-ports/){:target="_blank"}
