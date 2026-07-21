---
title: 'Google Launches Gemini 3.5 Flash Cyber AI to Find and Fix Software Vulnerabilities'
date: 2026-07-21
permalink: /posts/2026/07/21/google-launches-gemini-35-flash-cyber-ai-to-find-and-fix-software-vulnerabilities/
tags:
- veille-cyber
- hackernews
---
### Lancement de Gemini 3.5 Flash Cyber pour la cybersécurité automatisée

Google DeepMind a dévoilé **Gemini 3.5 Flash Cyber**, un modèle d'intelligence artificielle spécialisé dans la détection, la validation et la correction automatisée de vulnérabilités logicielles. Intégré à l'agent **CodeMender**, ce modèle léger est conçu pour être à la fois rapide et économiquement avantageux, surpassant ses prédécesseurs et ses concurrents (tels que Claude Opus 4.6) lors d'analyses complexes sur des projets d'envergure comme le moteur V8 JavaScript.

**Points clés :**
*   **Accès restreint :** Pour prévenir les risques de double usage, le modèle est actuellement réservé aux gouvernements et partenaires de confiance via CodeMender.
*   **Performance supérieure :** Lors de tests, le modèle a identifié 55 vulnérabilités uniques dans le moteur V8, contre 47 pour Gemini 3.5 Flash et 36 pour Claude Opus 4.6, incluant des failles inédites.
*   **Capacités offensives simulées :** Le modèle a démontré sa capacité à générer des exploits fonctionnels de type exécution de code à distance (RCE), capables de contourner des mécanismes de défense standard comme l'ASLR et le W^X.
*   **Stratégie de déploiement :** Google utilise des barrières de sécurité (guardrails) strictes au sein de CodeMender pour permettre les analyses de défense tout en empêchant toute utilisation malveillante.

**Vulnérabilités testées :**
*   Exécution de code à distance (RCE) dans des API publiques.
*   Corruption de mémoire (Memory-corruption) dans des services de production sensibles.
*   *Note : Aucune CVE spécifique n'a été mentionnée dans l'article, le modèle se concentrant sur la découverte de nouvelles failles.*

**Recommandations :**
*   **Usage encadré :** Privilégier l'intégration d'outils d'IA via des plateformes sécurisées et contrôlées (type *Gemini Enterprise Agent Platform*) pour minimiser les risques de détournement.
*   **Défense proactive :** Tirer parti de l'IA pour automatiser le cycle "découverte-correction" afin de réduire la fenêtre d'exposition entre l'apparition d'une faille et sa remédiation.
*   **Red-teaming :** Utiliser ces capacités de modélisation pour renforcer les tests d'intrusion sur les infrastructures critiques avant un déploiement public.

---
[Source](https://thehackernews.com/2026/07/google-launches-gemini-35-flash-cyber.html){:target="_blank"}
