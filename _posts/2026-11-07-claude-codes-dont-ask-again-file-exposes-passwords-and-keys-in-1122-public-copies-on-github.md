---
title: 'Claude Codes “Dont Ask Again” File Exposes Passwords and Keys in 1,122 Public Copies on GitHub'
date: 2026-11-07
permalink: /posts/2026/11/07/claude-codes-dont-ask-again-file-exposes-passwords-and-keys-in-1122-public-copies-on-github/
tags:
- veille-cyber
- hackernews
---
### Fuite massive de secrets via Claude Code sur GitHub

L'assistant de programmation IA « Claude Code » d'Anthropic expose involontairement des mots de passe, clés d'API et jetons d'authentification. En utilisant la fonctionnalité « Don't ask again » (Ne plus demander), l'outil enregistre les commandes saisies par l'utilisateur — incluant les secrets — en texte clair dans le fichier `.claude/settings.local.json`. Ces fichiers sont fréquemment poussés par erreur sur des dépôts GitHub publics, où ils sont indexés.

**Points clés :**
*   **Volumétrie :** 1 122 fichiers publics contiennent au moins un secret, totalisant plus de 2 500 identifiants compromis (clés AWS, accès bases de données, jetons SSH/npm).
*   **Persistance :** La suppression du fichier ne suffit pas, car les secrets restent accessibles dans l'historique Git et les forks des dépôts.
*   **Défaut de conception :** Claude Code ne s'ajoute pas automatiquement au `.gitignore` du projet, rendant les fichiers de configuration vulnérables aux commits accidentels.
*   **Réaction absente :** Des rapports de bugs signalant ce problème depuis août 2025 ont été fermés par des bots sans intervention d'Anthropic.

**Vulnérabilités :**
*   **Exposition de secrets en clair :** Le fichier `settings.local.json` stocke les commandes complètes, incluant les identifiants saisis par l'utilisateur.
*   **Absence d'exclusion Git :** Le fichier n'est pas protégé par défaut au niveau du dépôt, seulement localement via des exclusions globales utilisateur, inefficaces lors du partage du code.

**Recommandations :**
*   **Pour les développeurs :**
    *   Révoquer et renouveler immédiatement tous les identifiants présents dans ces fichiers.
    *   Scanner l'historique complet des dépôts (y compris les fichiers supprimés) pour détecter `.claude/settings.local.json`.
    *   Ajouter manuellement ce fichier au `.gitignore` du projet.
    *   Privilégier l'utilisation de variables d'environnement pour gérer les secrets plutôt que de les inclure dans les commandes.
*   **Pour les équipes de sécurité :**
    *   Inclure les dossiers de configuration des outils IA (`.claude/`, `.cursor/`, etc.) dans les scans de secrets CI/CD.
    *   Configurer les outils de détection (Gitleaks, TruffleHog) pour repérer non seulement les formats de clés connus, mais aussi les mots de passe saisis dans des lignes de commande.

---
[Source](https://thehackernews.com/2026/11/claude-codes-dont-ask-again-file.html){:target="_blank"}
