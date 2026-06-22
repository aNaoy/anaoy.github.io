---
title: 'Microsoft fixes AutoGen Studio flaw that enabled code execution'
date: 2026-06-22
permalink: /posts/2026/06/22/microsoft-fixes-autogen-studio-flaw-that-enabled-code-execution/
tags:
- veille-cyber
- bleepingcomp
---
### AutoJack : Vulnérabilité critique de RCE dans AutoGen Studio

Microsoft a identifié et corrigé une chaîne de vulnérabilités, baptisée **AutoJack**, affectant l'interface AutoGen Studio. Cette faille permettait à un attaquant d'exécuter des commandes arbitraires sur le système hôte via l'interface des agents IA. L'impact a été limité aux développeurs ayant compilé le code source depuis la branche principale de GitHub durant une courte période ; les versions publiées sur PyPI n'ont jamais été exposées.

**Points clés :**
*   **Mécanisme d'attaque :** Un attaquant incite l'agent IA d'un développeur à visiter une page web malveillante. Le script injecté établit une connexion WebSocket avec l'interface locale d'AutoGen Studio pour exécuter des commandes.
*   **Portée :** Concerne uniquement les versions compilées depuis GitHub avant le correctif (commit `b047730`). Aucune CVE n'a été assignée car le correctif a été appliqué avant toute mise en production publique.

**Vulnérabilités techniques :**
1.  **Confiance aveugle locale :** Le WebSocket MCP faisait confiance aux connexions provenant de `localhost`, facilitant l'usurpation de sources locales.
2.  **Défaut d'authentification :** Les routes `/api/mcp/*` contournaient les contrôles d'authentification, rendant le point de terminaison accessible sans justificatifs.
3.  **Injections de commandes :** Le paramètre `server_params` encodé en base64 était transmis directement au processus de lancement, permettant l'exécution arbitraire de commandes Bash, PowerShell ou d'exécutables.

**Recommandations :**
*   **Isolation :** Déployer AutoGen Studio exclusivement dans des environnements isolés (conteneurs ou machines virtuelles) sans accès direct à Internet.
*   **Privilèges restreints :** Exécuter l'application sous un compte utilisateur aux droits limités, distinct du compte personnel quotidien.
*   **Usage prudent :** Éviter de permettre à des agents IA ayant accès au web d'interagir avec des composants capables d'exécuter du code local sur des machines sensibles.
*   **Mise à jour :** S'assurer d'utiliser les dernières versions stables publiées sur PyPI.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-fixes-autogen-studio-flaw-that-enabled-code-execution/){:target="_blank"}
