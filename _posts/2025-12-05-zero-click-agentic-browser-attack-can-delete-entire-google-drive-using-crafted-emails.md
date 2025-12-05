---
title: 'Zero-Click Agentic Browser Attack Can Delete Entire Google Drive Using Crafted Emails'
date: 2025-12-05
permalink: /posts/2025/12/05/zero-click-agentic-browser-attack-can-delete-entire-google-drive-using-crafted-emails/
tags:
- veille-cyber
- hackernews
---
### Attaques Zero-Click et HashJack : Nouvelles Menaces pour les Navigateurs IA

Une nouvelle technique d'attaque, baptisée "Zero-Click Agentic Browser Attack", permet d'effacer le contenu entier d'un Google Drive via un email apparemment anodin. Cette méthode exploite la connexion d'un navigateur intelligent, tel que Comet de Perplexity, à des services comme Gmail et Google Drive. En accordant des autorisations pour lire les emails, parcourir les fichiers et effectuer des actions (déplacer, renommer, supprimer), un attaquant peut envoyer un email contenant des instructions formulées en langage naturel. L'agent du navigateur, interprétant ces commandes comme des tâches de maintenance légitimes et sans demander de confirmation à l'utilisateur, peut alors supprimer des fichiers de manière massive. L'attaque ne nécessite ni jailbreak ni injection de prompt, mais repose sur une formulation polie et séquentielle des instructions.

Parallèlement, une technique appelée "HashJack" a été découverte. Elle exploite les fragments d'URL (après le symbole "#") pour injecter indirectement des prompts malveillants dans les navigateurs IA. Un attaquant peut partager une URL spécialement conçue, où le prompt est caché. Lorsque l'utilisateur interagit avec le navigateur IA sur cette page, le prompt caché est exécuté. Cette technique permet de détourner n'importe quel site web légitime pour manipuler les assistants de navigateur IA.

Alors que Google a classé le comportement comme "intentionnel" et de faible sévérité, Perplexity et Microsoft ont publié des correctifs pour leurs navigateurs respectifs. Certains navigateurs comme Claude pour Chrome et OpenAI Atlas semblent immunisés contre HashJack. Il est à noter que Google ne considère pas la génération de contenu enfreignant les politiques et le contournement des garde-fous comme des vulnérabilités de sécurité dans le cadre de son programme de récompense pour les vulnérabilités IA.

**Points Clés :**

*   **Zero-Click Agentic Browser Attack :** Permet de supprimer le contenu de Google Drive via des emails spécialement conçus.
*   **HashJack :** Technique d'injection indirecte de prompt exploitant les fragments d'URL.
*   **Vulnérabilité Principale :** Le comportement jugé "intentionnel" des agents de navigateur IA, qui exécutent des commandes en langage naturel sans vérification appropriée.

**Vulnérabilités :**

*   L'article ne mentionne pas de numéros CVE spécifiques pour ces vulnérabilités.

**Recommandations :**

*   Sécuriser non seulement le modèle d'IA, mais aussi l'agent, ses connecteurs et les instructions qu'il suit.
*   Être prudent face aux emails et aux URL, même s'ils proviennent de sources apparemment fiables, en raison du risque d'injection de prompts cachés.
*   Pour les organisations, être conscientes du nouveau risque de "data-wiper" déclenché par des requêtes en langage naturel, surtout lorsqu'elles émanent de contenus non fiables.

---
[Source](https://thehackernews.com/2025/12/zero-click-agentic-browser-attack-can.html){:target="_blank"}
