---
title: 'How to scan for vulnerabilities with GitHub Security Lab’s open source AI-powered framework'
date: 2026-03-07
permalink: /posts/2026/03/07/how-to-scan-for-vulnerabilities-with-github-security-labs-open-source-ai-powered-framework/
tags:
- veille-cyber
- zerodaysfans
---
### Automatisation de la recherche de vulnérabilités par IA via "Taskflows"

Le GitHub Security Lab a développé un framework open source basé sur des agents IA (LLM), appelé **Taskflows**, capable d'analyser automatiquement des bases de code pour identifier des vulnérabilités de sécurité complexes, notamment celles liées à la logique métier, souvent ignorées par les outils d'analyse statique (SAST) classiques.

**Points clés :**
*   **Approche méthodologique :** Contrairement à une requête unique, le framework décompose l'audit en étapes séquentielles (modélisation des menaces, identification des points d'entrée, suggestion de vulnérabilités, puis audit rigoureux).
*   **Gestion des hallucinations :** Le système utilise des instructions strictes, des critères de validation contextuels (modèle de menace, intentions du composant) et exige des preuves concrètes dans le code (fichiers/lignes).
*   **Efficacité :** Le framework a permis de rapporter plus de 80 vulnérabilités avec un taux élevé de "vrais positifs" sur des failles logiques (IDOR, contrôle d'accès).
*   **Accessibilité :** L'outil est disponible sur le dépôt [seclab-taskflows](https://github.com/GitHubSecurityLab/seclab-taskflows) et nécessite une licence GitHub Copilot.

**Vulnérabilités majeures identifiées :**
*   **CVE-2025-64487 (Outline) :** Élévation de privilèges permettant à un utilisateur standard de modifier les permissions de groupes sur des documents.
*   **CVE-2025-15033 (WooCommerce) :** Divulgation d'informations personnelles (PII) permettant à des utilisateurs connectés de consulter des commandes d'invités.
*   **CVE-2026-25758 & CVE-2026-25757 (Spree Commerce) :** Fuite de données personnelles via l'énumération séquentielle d'identifiants de commandes.
*   **CVE-2026-28514 (Rocket.Chat) :** Contournement complet de l'authentification par mot de passe dû à une mauvaise gestion des promesses (Promises) en JavaScript, rendant la condition `if (!valid)` toujours vraie.

**Recommandations :**
*   **Audits ciblés :** Utiliser les *Taskflows* pour automatiser la recherche de vulnérabilités logiques qui échappent aux outils de balayage classiques.
*   **Réitération :** Effectuer plusieurs passes d'audit sur une même base de code avec différents modèles de langage pour varier les angles d'analyse.
*   **Modélisation des menaces :** S'assurer que l'outil est configuré pour comprendre les frontières de sécurité et les usages prévus du code afin de limiter les faux positifs.
*   **Contribution :** Collaborer à l'écosystème open source en créant des *Taskflows* personnalisés pour des besoins spécifiques ou des types de vulnérabilités particuliers.

---
[Source](https://github.blog/security/how-to-scan-for-vulnerabilities-with-github-security-labs-open-source-ai-powered-framework/){:target="_blank"}
