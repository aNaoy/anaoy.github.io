---
title: 'Researchers Trick Perplexitys Comet AI Browser Into Phishing Scam in Under Four Minutes'
date: 2026-03-11
permalink: /posts/2026/03/11/researchers-trick-perplexitys-comet-ai-browser-into-phishing-scam-in-under-four-minutes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des navigateurs IA : La menace de l'« Agentic Blabbering »

Les navigateurs dotés d'agents d'intelligence artificielle (IA), conçus pour exécuter des tâches autonomes, présentent une nouvelle surface d'attaque critique : les attaquants ne cherchent plus à tromper l'utilisateur humain, mais directement le modèle d'IA lui-même.

**Points clés :**
*   **Agentic Blabbering :** Le comportement verbeux des agents IA, qui décrivent en temps réel leurs processus de raisonnement et leurs hésitations face à une page web, fournit des données précieuses aux attaquants.
*   **Apprentissage adversarial :** En utilisant ces retours comme signaux d'entraînement, les attaquants peuvent optimiser leurs sites de phishing via des réseaux antagonistes génératifs (GAN) jusqu'à ce que le navigateur IA les valide systématiquement.
*   **Intent Collision :** Une technique d'injection où l'IA fusionne une demande légitime de l'utilisateur avec des instructions malveillantes dissimulées sur une page web, rendant la distinction entre les deux impossible pour le modèle.
*   **Ciblage industrialisé :** Une fois qu'une arnaque est entraînée avec succès pour contourner un modèle d'IA spécifique, elle devient immédiatement efficace contre tous les utilisateurs de ce navigateur.

**Vulnérabilités identifiées (sans CVE spécifique) :**
*   **PerplexedBrowser :** Failles de type "zero-click" permettant l'exfiltration de fichiers locaux ou la compromission de coffres-forts (ex: 1Password).
*   **Injection de prompts indirecte :** Exploitation via des contenus web malveillants (e-mails, invitations) pour détourner les actions de l'agent.
*   **Extraction de données :** Utilisation de l'IA pour accéder à des informations privées (ex: Gmail) lors de requêtes de résumé de pages web contrôlées par l'attaquant.

**Recommandations :**
*   **Entraînement adversarial :** Les éditeurs doivent renforcer leurs modèles en simulant des attaques automatisées en phase de développement.
*   **Limitation du "Blabbering" :** Réduire la transparence excessive du raisonnement interne de l'agent lorsqu'il interagit avec des domaines non fiables.
*   **Sécurisation au niveau système :** Implémenter des garde-fous plus stricts au niveau du navigateur pour isoler les instructions système des données provenant de sources externes, bien que la résolution complète de ces vulnérabilités demeure un défi complexe pour l'industrie.

---
[Source](https://thehackernews.com/2026/03/researchers-trick-perplexitys-comet-ai.html){:target="_blank"}
