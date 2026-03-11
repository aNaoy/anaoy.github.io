---
title: 'Researchers Trick Perplexitys Comet AI Browser Into Phishing Scam in Under Four Minutes'
date: 2026-03-11
permalink: /posts/2026/03/11/researchers-trick-perplexitys-comet-ai-browser-into-phishing-scam-in-under-four-minutes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des navigateurs IA : Le risque du "Agentic Blabbering"

Les navigateurs autonomes basés sur l'IA, comme Comet de Perplexity, sont vulnérables à des techniques d'ingénierie sociale automatisées. Le passage de l'interaction humaine à l'autonomie des agents IA déplace la surface d'attaque : les cybercriminels ne cherchent plus à tromper l'utilisateur, mais à manipuler le modèle d'IA lui-même pour contourner ses barrières de sécurité.

**Points clés :**
*   **Agentic Blabbering :** Le processus de raisonnement des navigateurs IA est trop explicite. En interceptant les données que l'IA communique sur ses réflexions et ses soupçons, un attaquant peut entraîner une IA malveillante à optimiser ses tentatives de hameçonnage jusqu'à ce que le navigateur cible les accepte comme sûres.
*   **Injections de requêtes (Prompt Injection) :** Des vulnérabilités permettent de fusionner des instructions malveillantes dissimulées (ex: dans un email ou une page web) avec les requêtes légitimes de l'utilisateur.
*   **Évolutivité des attaques :** Une fois qu'un piège est optimisé pour un modèle d'IA spécifique, il devient universellement efficace contre tous les utilisateurs de ce navigateur.

**Vulnérabilités identifiées :**
*   **PerplexedBrowser :** Une série de failles (attaques "zero-click") ayant permis l'exfiltration de fichiers locaux et le détournement de comptes de gestionnaires de mots de passe (ex: 1Password).
*   **Techniques d'injection :** Diverses méthodes de *prompt injection* et d'« intent collision » (conflit d'intention) exploitées pour accéder aux données privées (Gmail, fichiers locaux).
*   *Note : Aucune CVE spécifique n'est mentionnée pour ces recherches, car elles portent sur des failles logiques inhérentes au fonctionnement des LLM (Large Language Models) plutôt que sur des erreurs de code classiques.*

**Recommandations :**
*   **Adoption de garde-fous système :** Mise en œuvre de couches de sécurité au niveau du système d'exploitation et du navigateur pour isoler les agents IA.
*   **Entraînement contradictoire :** Soumettre les modèles d'IA à des tests de stress automatisés utilisant des attaques par apprentissage pour identifier les vulnérabilités avant le déploiement.
*   **Prudence opérationnelle :** Garder à l'esprit que les agents autonomes ne sont pas encore totalement sécurisés contre les manipulations malveillantes et limiter leur accès aux données sensibles ou aux sessions authentifiées (banque, gestionnaires de mots de passe).

---
[Source](https://thehackernews.com/2026/03/researchers-trick-perplexitys-comet-ai.html){:target="_blank"}
