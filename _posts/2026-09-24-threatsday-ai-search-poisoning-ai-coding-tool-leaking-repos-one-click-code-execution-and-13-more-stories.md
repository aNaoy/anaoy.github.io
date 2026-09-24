---
title: 'ThreatsDay: AI Search Poisoning, AI Coding Tool Leaking Repos, One-Click Code Execution and 13 More Stories'
date: 2026-09-24
permalink: /posts/2026/09/24/threatsday-ai-search-poisoning-ai-coding-tool-leaking-repos-one-click-code-execution-and-13-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces hebdomadaires : L'essor de l'IA malveillante et l'exploitation des comportements de confiance

Le paysage des cybermenaces est marqué par une montée en puissance de l'utilisation de l'intelligence artificielle pour automatiser les attaques, couplée à une exploitation croissante des outils de développement et des mécanismes de confiance.

**Points clés :**
*   **Empoisonnement de l'IA :** Les résultats des moteurs de recherche basés sur l'IA sont détournés pour diffuser de fausses informations, des numéros de support frauduleux et des pages de phishing ciblant de grandes entreprises.
*   **Fuites de données par les outils IA :** Plusieurs assistants de code ont été épinglés pour avoir téléchargé automatiquement des dépôts de code privés vers des clouds tiers sans consentement explicite.
*   **Attaques sur la Supply Chain :** Des dépendances malveillantes sont insérées dans des projets populaires (ex: *Deep-Live-Cam*) pour déployer des infostealers ou des chevaux de Troie.
*   **Évolution des tactiques :** Les attaquants délaissent de plus en plus les exploits complexes (0-day) au profit de l'ingénierie sociale simple et de l'exploitation de mauvaises configurations, rendant les attaques plus accessibles et fréquentes.

**Vulnérabilités notables :**
*   **Process Parameter Poisoning :** Nouvelle technique d'évasion EDR injectant du code durant l'initialisation d'un processus sans utiliser les API classiques.
*   **Contournement de "Workspace Trust" (VS Code) :** Une faille permet via un lien piégé de forcer l'exécution de code sur la machine de la victime en contournant les protections de confiance de l'éditeur.
*   **CVE-2023-38831 et CVE-2024-21412 :** Bien que des vulnérabilités connues, elles restent des références dans l'évolution des malwares comme *DarkMe*, bien que ces derniers s'orientent désormais vers des vecteurs moins techniques.

**Recommandations :**
*   **Appliquer le Principe du Moindre Privilège (PoLP) :** Restreindre strictement les accès accordés aux tiers (intégrateurs ICS) et aux outils de développement (ex: utiliser *cache-mode* pour GitHub Actions).
*   **Vigilance sur les outils tiers :** Auditer les réglages par défaut des outils IA utilisés en entreprise pour éviter l'exfiltration involontaire de code source.
*   **Renforcement de la sensibilisation :** Étant donné l'efficacité croissante des attaques "Browser-in-the-Browser" (BitB) et du phishing, renforcer la formation des utilisateurs aux signaux d'alerte (URL suspectes, fenêtres de connexion incohérentes).
*   **Mise à jour proactive :** Suivre les cycles de correctifs accélérés, notamment pour les infrastructures critiques et les noyaux Linux, afin de réduire la fenêtre d'exposition aux vulnérabilités connues.

---
[Source](https://thehackernews.com/2026/09/threatsday-ai-search-poisoning-ai.html){:target="_blank"}
