---
title: 'Claude Opus 5 Helped Researchers Take Over OpenAI Staff Accounts via Chained Flaws'
date: 2026-09-19
permalink: /posts/2026/09/19/claude-opus-5-helped-researchers-take-over-openai-staff-accounts-via-chained-flaws/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque assistée par IA : compromission des accès internes d'OpenAI

Des chercheurs de la firme Hacktron ont démontré la possibilité d'utiliser l'IA (Claude Opus 5) pour enchaîner des vulnérabilités et compromettre les comptes de plusieurs employés d'OpenAI. L'attaque a permis d'accéder à des outils internes, dont des dépôts de code, en exploitant une faille sur un forum public lié aux systèmes d'authentification de l'entreprise.

**Points clés :**
*   **Utilisation de l'IA :** Le modèle Claude Opus 5 a été utilisé pour automatiser la création d'un exploit capable de contourner les protections mémoire (ASLR) en quelques heures.
*   **Vecteur d'attaque :** La compromission a débuté par l'exploitation d'une faille dans la bibliothèque de traitement d'images `libheif`, utilisée par le logiciel Discourse du forum d'OpenAI.
*   **SSO comme vecteur de mouvement latéral :** L'utilisation du même système d'authentification unique (SSO) pour le forum public et les services internes (ChatGPT, Codex, GitHub, Slack) a permis de passer d'un serveur tiers à l'infrastructure interne d'OpenAI.
*   **Nature de l'opération :** Il s'agissait d'une recherche de sécurité éthique. OpenAI a corrigé la faille en 14 heures et récompensé les chercheurs par une prime de 6 500 $.

**Vulnérabilité identifiée :**
*   **CVE-2026-32882 :** Faille dans `libheif` permettant une lecture hors limites (out-of-bounds read), utilisée ici pour corrompre la mémoire et parvenir à une exécution de code à distance (RCE) sur le serveur.

**Recommandations :**
*   **Mise à jour logicielle :** Mettre à jour `libheif` vers la version la plus récente (1.23.4 ou supérieure). Ne pas se limiter à une mise à jour applicative, mais reconstruire les images système utilisant des bibliothèques obsolètes.
*   **Isolation du traitement d'images :** Désactiver le décodage d'images non fiables (HEIF/AVIF) ou isoler les processus de traitement dans des environnements "sandbox" restreints.
*   **Gestion des identités :** Séparer les périmètres d'authentification. Éviter d'utiliser un SSO partagé entre des services publics à faible niveau de confiance et des outils internes sensibles. Exiger une authentification renforcée avant d'effectuer des actions critiques.

---
[Source](https://thehackernews.com/2026/09/claude-opus-5-helped-researchers-take.html){:target="_blank"}
