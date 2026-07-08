---
title: 'The GitHub Actions Attack Pattern Your CI Security Scanners Miss'
date: 2026-07-08
permalink: /posts/2026/07/08/the-github-actions-attack-pattern-your-ci-security-scanners-miss/
tags:
- veille-cyber
- bleepingcomp
---
### La menace invisible des workflows GitHub Actions : La faille « Cordyceps »

La recherche menée par Novee Security sur la vulnérabilité baptisée « Cordyceps » révèle une faille structurelle dans les pipelines CI/CD : le problème ne réside pas dans une ligne de code isolée, mais dans la composition logique des workflows GitHub Actions. Bien que les outils de scan (SAST/DAST) valident ces fichiers comme « sains », les enchaînements de privilèges permettent à des attaquants externes de détourner des processus automatisés pour obtenir des accès persistants ou voler des secrets.

**Points clés :**
*   **Absence de CVE :** Cordyceps n'étant pas une vulnérabilité logicielle classique mais une erreur de configuration systémique, elle échappe aux bases de données CVE et aux scanners de sécurité traditionnels.
*   **Mécanisme d'attaque :** L'exploitation repose sur l'utilisation des déclencheurs `pull_request_target` ou `workflow_run`. Ces derniers s'exécutent avec les privilèges du dépôt de base et l'accès aux secrets, contrairement aux `pull_request` standards.
*   **Effet multiplicateur de l'IA :** Les outils de codage par IA génèrent rapidement des configurations de CI/CD reproduisant ces schémas non sécurisés à grande échelle, rendant les audits humains obsolètes par leur volume.
*   **Impact :** Des organisations majeures (Microsoft, Google, Apache) ont été exposées, permettant potentiellement l'injection de code malveillant dans des mises à jour logicielles de confiance (supply chain attack).

**Vulnerabilités identifiées :**
*   **Injection de commande :** Interpolation de données contrôlées par l'attaquant (nom de branche, commentaires) directement dans des scripts shell.
*   **Injection de code :** Utilisation de `actions/github-script` pour évaluer des entrées externes comme du JavaScript.
*   **Escalade de privilèges inter-workflows :** Un workflow à bas privilèges transmet des données corrompues à un workflow à hauts privilèges, lequel utilise alors les jetons (tokens) du mainteneur pour exécuter des actions malveillantes.

**Recommandations :**
*   **Privilégier `pull_request` :** Éviter autant que possible `pull_request_target` pour les contributions externes.
*   **Isolation :** Ne jamais extraire (checkout) le code source d'une pull request au sein d'un workflow disposant de privilèges élevés ou d'accès aux secrets.
*   **Sécurisation des entrées :** Passer les données d'événement via des variables d'environnement citées plutôt que par insertion directe dans le shell.
*   **Gestion des permissions :** Appliquer le principe du moindre privilège par défaut (accès en lecture seule).
*   **Provenance :** Épingler les actions tierces à un hash de commit (SHA) plutôt qu'à un tag et soumettre les workflows critiques à une approbation manuelle pour les nouveaux contributeurs.
*   **Gouvernance :** Automatiser le contrôle de provenance des composants entrant dans le pipeline pour s'assurer qu'ils proviennent de sources vérifiées plutôt que d'une confiance aveugle.

---
[Source](https://www.bleepingcomputer.com/news/security/the-github-actions-attack-pattern-your-ci-security-scanners-miss/){:target="_blank"}
