---
title: 'SleeperGem Uses Three Malicious RubyGems Packages to Target Developer Machines'
date: 2026-07-20
permalink: /posts/2026/07/20/sleepergem-uses-three-malicious-rubygems-packages-to-target-developer-machines/
tags:
- veille-cyber
- hackernews
---
### SleeperGem : Une attaque sophistiquée sur la supply chain RubyGems

La campagne « SleeperGem » cible l'écosystème Ruby en détournant des comptes développeurs inactifs pour injecter des charges malveillantes dans des packages légitimes. Cette attaque de type « supply chain » vise spécifiquement les postes de travail des développeurs en évitant les environnements d'intégration continue (CI).

**Points clés :**
*   **Mode opératoire :** Les attaquants prennent le contrôle de comptes RubyGems dormants depuis des années pour publier des versions vérolées sans aucune trace dans les dépôts sources (GitHub).
*   **Ciblage :** Les malwares détectent la présence de variables d'environnement CI (Jenkins, GitHub Actions, etc.) pour s'auto-exclure et garantir qu'ils ne s'exécutent que sur des machines de développement.
*   **Persistence :** Les versions malveillantes téléchargent des scripts et des binaires depuis une instance Forgejo. Ils installent des démons en arrière-plan, utilisent des tâches Cron et tentent une élévation de privilèges (via `sudo`) pour planter un shell `setuid root`.
*   **Propagation :** Le package `git_credential_manager` (usurpant le nom de l'outil officiel Microsoft) a été ajouté comme dépendance à d'autres bibliothèques populaires, maximisant ainsi l'impact.

**Vulnérabilités :**
Aucune CVE n'est associée, car il s'agit d'une compromission de comptes de mainteneurs et d'une injection de code malveillant volontaire dans les paquets :
*   `git_credential_manager` (v2.8.0 à 2.8.3)
*   `Dendreo` (v1.1.3, 1.1.4)
*   `fastlane-plugin-run_tests_firebase_testlab` (v0.3.2)
*   *Autres paquets impactés par dépendance :* `slackHtmlToMarkdown`, `seo_optimizer`, `array_fast_methods`.

**Recommandations :**
*   **Réinitialisation immédiate :** Si vous avez utilisé ces packages, considérez votre machine et toutes les clés secrètes/identifiants qui y sont stockés comme compromis. Procédez à une rotation complète de tous les jetons et mots de passe.
*   **Nettoyage manuel :**
    *   Supprimer le répertoire du démon malveillant : `~/.local/share/gcm/`.
    *   Vérifier et supprimer les entrées de persistance (cron, systemd).
    *   Rechercher la présence du shell usurpé dans `/usr/local/sbin/ping6` et le supprimer.
*   **Sécurité des comptes :** Pour les mainteneurs, l'activation de l'authentification multifacteur (MFA) sur les comptes RubyGems est impérative pour prévenir le détournement de comptes inactifs.

---
[Source](https://thehackernews.com/2026/07/sleepergem-uses-three-malicious.html){:target="_blank"}
