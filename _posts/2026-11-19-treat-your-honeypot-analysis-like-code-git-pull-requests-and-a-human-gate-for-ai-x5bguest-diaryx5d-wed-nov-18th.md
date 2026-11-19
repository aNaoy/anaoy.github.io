---
title: 'Treat Your Honeypot Analysis Like Code: Git, Pull Requests and a Human Gate for AI &#x5b;Guest Diary&#x5d;, (Wed, Nov 18th)'
date: 2026-11-19
permalink: /posts/2026/11/19/treat-your-honeypot-analysis-like-code-git-pull-requests-and-a-human-gate-for-ai-x5bguest-diaryx5d-wed-nov-18th/
tags:
- veille-cyber
- sans-isc
---
### Analyse sécurisée de honeypots par le contrôle de version et l'IA

L'approche décrite consiste à traiter l'analyse des logs de honeypots comme du code source, en utilisant Git pour garantir la reproductibilité, la sécurité des données et la traçabilité des interventions de l'intelligence artificielle (IA).

**Points clés :**
*   **Workflow reproductible :** Chaque rapport d'attaque inclut les preuves brutes, les requêtes (ex: `jq`) utilisées pour l'extraction et une liste de hachages pour vérifier l'intégrité des données.
*   **Sécurité des données :** Un processus de filtrage systématique et automatisé remplace les informations sensibles (IP du capteur, noms d'hôte) avant tout commit pour éviter les fuites accidentelles.
*   **Gouvernance de l'IA :** L'IA (Claude Code) dispose d'une identité propre. Elle est autorisée à soumettre des rapports via des *pull requests*, mais n'a aucun droit de fusion (*merge*). La validation humaine est obligatoire.
*   **Transparence :** L'historique Git documente précisément le travail accompli par l'IA et les corrections apportées par l'humain, offrant une piste d'audit claire pour chaque affirmation sécuritaire.

**Vulnérabilité identifiée :**
*   **CVE-2026-109618 :** Tentative d'exploitation de type PHP2Shell via une requête POST multipart surdimensionnée, détectée lors de la surveillance des vulnérabilités PHP.

**Recommandations :**
*   **Imposer une revue humaine :** Ne jamais autoriser une IA à fusionner des changements dans la branche principale (*main*).
*   **Utiliser des checklists :** Intégrer un template de *pull request* incluant une vérification manuelle de la présence potentielle de secrets ou d'informations identifiables (PII/données système).
*   **Automatiser la détection de secrets :** Utiliser systématiquement des outils comme `gitleaks` avant chaque commit pour prévenir l'exposition de clés privées ou d'informations sensibles.
*   **Sécuriser les dépôts :** Configurer des règles strictes sur le serveur de gestion de code (GitHub) pour bloquer les *force-pushes* et imposer une approbation obligatoire par un tiers humain.

---
[Source](https://isc.sans.edu/diary/rss/33534){:target="_blank"}
