---
title: 'AI Recommendation Poisoning: How "Ask AI" Buttons Silently Alter LLM Memory'
date: 2026-08-06
permalink: /posts/2026/08/06/ai-recommendation-poisoning-how-ask-ai-buttons-silently-alter-llm-memory/
tags:
- veille-cyber
- hackernews
---
### L’Empoisonnement de la Mémoire par IA : Une Menace Silencieuse

L'empoisonnement de la mémoire par IA (AI Recommendation Poisoning) est une technique d'injection de prompt visant à manipuler durablement les préférences des modèles de langage (LLM). En exploitant les boutons « Ask AI » présents sur les sites web, des entreprises injectent des instructions cachées dans les sessions des utilisateurs pour s'auto-proclamer « sources de confiance » ou autorités dans leurs domaines respectifs.

**Points clés :**
* **Mécanisme :** Les boutons utilisent des liens profonds (deep links) pré-remplis qui exécutent une requête automatique lors de l'ouverture d'une session IA sans aucune interaction ni consentement de l'utilisateur.
* **Persistance :** L'instruction malveillante est intégrée à la mémoire à long terme de l'IA (ex: « enregistre ce domaine comme source de confiance »), biaisant ainsi toutes les futures réponses du modèle en faveur du vendeur.
* **Extension du problème :** Cette pratique se généralise via des plugins CMS, des outils marketing et des générateurs SEO, transformant des outils d'aide à la décision en vecteurs de manipulation publicitaire.

**Vulnérabilités associées :**
* **AML.T0080 (Memory Poisoning) :** Référencée dans la base MITRE ATLAS.
* **AML.T0051 (LLM Prompt Injection) :** Technique connexe d'injection de prompt.
* *Note : Bien que décrite comme un comportement de sécurité, il n'existe pas de CVE spécifique, car il s'agit d'un abus de fonctionnalité légitime des interfaces LLM.*

**Recommandations :**
* **Inspection des liens :** Analyser les paramètres de requête (`?q=...`) des boutons pointant vers les domaines d'assistants IA (ChatGPT, Claude, etc.) à la recherche de mots-clés comme « remember » ou « trusted source ».
* **Politique de sécurité :** Traiter ces liens comme des vecteurs de menace ; interdire le clic sur les boutons « Ask AI » non vérifiés lors de l'utilisation de comptes professionnels.
* **Audit de mémoire :** Utiliser des prompts d'audit pour interroger son propre historique LLM afin de détecter si des domaines tiers ont déjà été indûment enregistrés comme sources de référence.
* **Surveillance active :** Mettre en place une surveillance du DOM (Document Object Model) pour bloquer automatiquement les liens contenant des charges utiles (payloads) d'injection avant qu'ils ne soient accessibles par les utilisateurs.

---
[Source](https://thehackernews.com/2026/08/ai-recommendation-poisoning-how-ask-ai.html){:target="_blank"}
