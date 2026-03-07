---
title: 'OpenAI Codex Security Scanned 1.2 Million Commits and Found 10,561 High-Severity Issues'
date: 2026-03-07
permalink: /posts/2026/03/07/openai-codex-security-scanned-12-million-commits-and-found-10561-high-severity-issues/
tags:
- veille-cyber
- hackernews
---
### Lancement de Codex Security par OpenAI : Détection et correction automatisée des vulnérabilités

OpenAI a déployé **Codex Security**, un agent d'IA conçu pour identifier, valider et corriger les failles de sécurité dans le code source. Évolution de l'outil « Aardvark », cette solution analyse le contexte global des projets pour limiter les faux positifs et proposer des correctifs pertinents.

**Points clés :**
*   **Performance :** En 30 jours, plus de 1,2 million de commits ont été scannés, révélant 792 vulnérabilités critiques et 10 561 failles de haute sévérité.
*   **Méthodologie en trois étapes :**
    1.  Analyse structurelle et création d'un modèle de menace éditable.
    2.  Identification des vulnérabilités basée sur l'impact réel.
    3.  Validation par des tests en environnement isolé (*sandboxing*) et génération de preuves de concept.
*   **Disponibilité :** Accessible en préversion de recherche pour les clients ChatGPT Pro, Enterprise, Business et Edu.

**Vulnérabilités identifiées (exemples) :**
*   **GnuPG :** CVE-2026-24881, CVE-2026-24882
*   **GnuTLS :** CVE-2025-32988, CVE-2025-32989
*   **GOGS :** CVE-2025-64175, CVE-2026-25242
*   **Thorium :** CVE-2025-35430 à CVE-2025-35436

**Recommandations :**
*   Intégrer des agents d'IA capables de construire un contexte système approfondi pour réduire le « bruit » des alertes non critiques.
*   Privilégier les outils capables de valider les vulnérabilités dans des environnements isolés avant de soumettre les correctifs aux équipes de développement.
*   Utiliser les preuves de concept générées par l'IA pour accélérer la remédiation et valider l'impact des correctifs avant leur déploiement en production.

---
[Source](https://thehackernews.com/2026/03/openai-codex-security-scanned-12.html){:target="_blank"}
