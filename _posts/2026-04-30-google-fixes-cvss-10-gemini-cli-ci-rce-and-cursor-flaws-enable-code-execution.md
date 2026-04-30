---
title: 'Google Fixes CVSS 10 Gemini CLI CI RCE and Cursor Flaws Enable Code Execution'
date: 2026-04-30
permalink: /posts/2026/04/30/google-fixes-cvss-10-gemini-cli-ci-rce-and-cursor-flaws-enable-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les outils d'IA : Gemini CLI et Cursor sous surveillance

Des failles de sécurité majeures ont été identifiées dans **Google Gemini CLI** et l'IDE **Cursor**, permettant l'exécution de code à distance (RCE) sur les systèmes des utilisateurs et des serveurs CI/CD.

#### Points clés
*   **Gemini CLI :** Le mode "headless" (utilisé dans les pipelines CI/CD) faisait automatiquement confiance aux dossiers locaux, permettant à des attaquants de charger des configurations malveillantes via des fichiers `.gemini/` pour exécuter des commandes.
*   **Cursor (IDE) :** L'outil est vulnérable à une évasion de bac à sable via des dépôts Git piégés. L'agent IA, en exécutant des commandes Git légitimes, déclenche involontairement des *hooks* malveillants cachés dans des dépôts imbriqués.
*   **CursorJacking :** Une vulnérabilité supplémentaire permet aux extensions installées d'accéder aux clés API et jetons de session stockés localement dans une base SQLite non protégée.

#### Vulnérabilités identifiées
*   **Gemini CLI (RCE) :** Aucun identifiant CVE, score **CVSS 10.0** (critique). Concerne `@google/gemini-cli` < 0.39.1 / 0.40.0-preview.3 et `google-github-actions/run-gemini-cli` < 0.1.22.
*   **Cursor (Évasion de sandbox) :** **CVE-2026-26268**, score **CVSS 8.1**. Concerne les versions antérieures à 2.5.
*   **Cursor (Accès non autorisé) :** **CursorJacking** (sans CVE), score **CVSS 8.2**. Actuellement non corrigé.

#### Recommandations
*   **Pour Gemini CLI :**
    *   Mettre à jour vers les versions corrigées.
    *   Désactiver la confiance automatique dans les pipelines CI/CD.
    *   Utiliser la variable `GEMINI_TRUST_WORKSPACE: 'true'` uniquement sur des entrées fiables.
    *   Configurer les listes blanches (*allowlists*) de commandes autorisées lors de l'utilisation du mode `--yolo`.
*   **Pour Cursor :**
    *   Mettre à jour l'IDE vers la version 2.5 ou ultérieure.
    *   Faire preuve d'une extrême prudence lors de l'ouverture de dépôts tiers ou inconnus.
    *   N'installer que des extensions provenant de sources vérifiées et de confiance, en raison de l'absence de cloisonnement des accès aux données locales.

---
[Source](https://thehackernews.com/2026/04/google-fixes-cvss-10-gemini-cli-ci-rce.html){:target="_blank"}
