---
title: 'Previously harmless Google API keys now expose Gemini AI data'
date: 2026-02-27
permalink: /posts/2026/02/27/previously-harmless-google-api-keys-now-expose-gemini-ai-data/
tags:
- veille-cyber
- bleepingcomp
---
## Vulnérabilité des clés API Google : De innocentes à porte d'entrée pour Gemini

Des clés API Google, autrefois considérées comme inoffensives et intégrées au code côté client pour des services comme Google Maps, peuvent désormais être exploitées pour authentifier l'accès à l'assistant Gemini et compromettre des données privées. Ce changement de statut découle de l'intégration de l'API du grand modèle linguistique (LLM) Gemini aux projets Google Cloud.

**Points Clés :**

*   Des chercheurs ont identifié près de 3 000 clés API Google exposées publiquement sur internet.
*   Ces clés étaient intégrées dans le code source de sites web accessibles, souvent depuis des années, sans constituer un risque préalable.
*   L'introduction de Gemini a conféré à ces clés des privilèges d'authentification inattendus pour l'assistant IA.
*   Un attaquant peut copier une clé API depuis le code source d'une page web et l'utiliser pour interagir avec l'API Gemini.
*   L'utilisation de l'API Gemini n'étant pas gratuite, cela peut entraîner des coûts significatifs pour la victime, potentiellement des milliers de dollars par jour par compte compromis.

**Vulnérabilités :**

*   Il n'y a pas de CVE spécifique mentionné pour cette vulnérabilité. La faille est décrite comme une "escalade de privilèges sur un seul service" par Google.

**Recommandations :**

*   **Vérification et Audit :** Les développeurs doivent vérifier si l'API Gemini (API de Langage Génératif) est activée dans leurs projets. Ils doivent auditer toutes leurs clés API pour détecter toute exposition publique.
*   **Rotation Immédiate :** Les clés API trouvées exposées publiquement doivent être immédiatement révoquées et remplacées par de nouvelles.
*   **Utilisation d'Outils :** L'outil open-source TruffleHog est recommandé pour détecter les clés API exposées dans le code et les dépôts.
*   **Mesures Proactives de Google :** Google a mis en place des mesures pour détecter et bloquer les clés API compromises tentant d'accéder à Gemini. Les nouvelles clés de l'AI Studio auront par défaut une portée limitée à Gemini, et des notifications seront envoyées en cas de détection de fuites.

---
[Source](https://www.bleepingcomputer.com/news/security/previously-harmless-google-api-keys-now-expose-gemini-ai-data/){:target="_blank"}
