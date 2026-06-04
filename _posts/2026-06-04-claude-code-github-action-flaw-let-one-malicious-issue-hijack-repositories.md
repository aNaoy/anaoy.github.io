---
title: 'Claude Code GitHub Action Flaw Let One Malicious Issue Hijack Repositories'
date: 2026-06-04
permalink: /posts/2026/06/04/claude-code-github-action-flaw-let-one-malicious-issue-hijack-repositories/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Claude Code : Risque de détournement de dépôts GitHub

Une faille de sécurité découverte dans l'action GitHub « Claude Code » d'Anthropic permettait à des attaquants de prendre le contrôle complet de dépôts publics via une simple ouverture d'issue malveillante. Cette vulnérabilité, notée 7.8 sur l'échelle CVSS v4.0, exploitait une défaillance dans le mécanisme de vérification des permissions et une injection de prompt indirecte.

**Points clés :**
*   **Défaut de validation :** L'action considérait par erreur tout utilisateur dont le nom se terminait par `[bot]` comme une entité de confiance, permettant à n'importe quel attaquant possédant un GitHub App de déclencher l'IA.
*   **Injection de prompt :** En insérant des instructions malveillantes dans une issue, l'attaquant pouvait forcer Claude à lire des variables d'environnement (`/proc/self/environ`), accédant ainsi aux jetons d'authentification (OIDC).
*   **Escalade de privilèges :** Une fois les jetons obtenus, l'attaquant pouvait usurper l'identité de l'action pour modifier le code, les workflows ou les configurations du dépôt.
*   **Risque de chaîne d'approvisionnement :** Le risque était tel qu'un attaquant aurait pu injecter du code malveillant dans l'action elle-même, infectant ainsi tous les projets utilisant cette dépendance.

**Vulnérabilités :**
*   **Bypass de contrôle d'accès :** Validation insuffisante des déclencheurs (bots).
*   **Injection de prompt indirecte :** Manipulation de l'IA pour l'exfiltration de secrets via le contenu des issues.
*   **Configuration risquée :** Utilisation de `allowed_non_write_users: "*"` dans les workflows, exposant les systèmes aux utilisateurs non authentifiés.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **v1.0.94** (ou supérieure) de `claude-code-action`.
*   **Audit des accès :** Restreindre strictement les permissions des workflows GitHub aux utilisateurs ayant un accès en écriture.
*   **Sécurisation des secrets :** Ne jamais exposer de jetons sensibles ou de données environnementales aux entrées utilisateur non filtrées traitées par des agents IA.
*   **Nettoyage des workflows :** Supprimer les outils ou permissions non essentiels dans les automatisations basées sur l'IA pour limiter le rayon d'action en cas de compromission.

---
[Source](https://thehackernews.com/2026/06/claude-code-github-action-flaw-let-one.html){:target="_blank"}
