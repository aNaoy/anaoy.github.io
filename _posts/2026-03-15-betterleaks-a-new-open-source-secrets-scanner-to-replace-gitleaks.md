---
title: 'Betterleaks, a new open-source secrets scanner to replace Gitleaks'
date: 2026-03-15
permalink: /posts/2026/03/15/betterleaks-a-new-open-source-secrets-scanner-to-replace-gitleaks/
tags:
- veille-cyber
- bleepingcomp
---
### Betterleaks : La nouvelle génération de détection de secrets

Betterleaks est un nouvel outil open-source conçu par Zach Rice, créateur de Gitleaks, pour succéder à ce dernier. Développé avec le soutien d'Aikido Security, il vise à offrir une solution plus performante et précise pour identifier les identifiants, clés API et jetons accidentellement exposés dans les dépôts de code.

**Points clés :**
*   **Technologie avancée :** Utilisation de la tokenisation BPE (Byte Pair Encoding) au lieu de l'entropie, atteignant un rappel de 98,6 % contre 70,4 % pour les méthodes traditionnelles.
*   **Architecture optimisée :** Implémentation en pur Go (sans dépendance CGO ou Hyperscan) et support du scan parallélisé pour une analyse accélérée.
*   **Fonctionnalités intelligentes :** Validation via CEL (Common Expression Language), gestion automatique du double/triple encodage et intégration facilitée pour les workflows utilisant des agents IA.
*   **Gouvernance ouverte :** Projet sous licence MIT, maintenu par une équipe pluridisciplinaire (Aikido, Red Hat, Amazon, Royal Bank of Canada).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais met en évidence le risque critique lié à l'exposition de secrets (clés privées, tokens) dans les dépôts publics, une pratique exploitée activement par les attaquants pour compromettre les infrastructures.

**Recommandations :**
*   **Intégration proactive :** Déployer Betterleaks dans le cycle de développement pour scanner systématiquement les répertoires et fichiers avant toute poussée de code.
*   **Automatisation :** Exploiter les capacités de l'outil pour créer des pipelines de détection automatisés, capables d'analyser non seulement le code source, mais également les fichiers générés par l'IA.
*   **Veille et mise à jour :** Suivre les prochaines évolutions du projet, notamment les futures fonctionnalités d'analyse assistée par LLM et de révocation automatique des jetons via API.

---
[Source](https://www.bleepingcomputer.com/news/security/betterleaks-a-new-open-source-secrets-scanner-to-replace-gitleaks/){:target="_blank"}
