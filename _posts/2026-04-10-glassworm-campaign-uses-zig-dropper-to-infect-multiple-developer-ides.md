---
title: 'GlassWorm Campaign Uses Zig Dropper to Infect Multiple Developer IDEs'
date: 2026-04-10
permalink: /posts/2026/04/10/glassworm-campaign-uses-zig-dropper-to-infect-multiple-developer-ides/
tags:
- veille-cyber
- hackernews
---
### Propagation de malwares via extensions IDE : La campagne GlassWorm

La campagne malveillante « GlassWorm » a évolué en intégrant un *dropper* développé en langage Zig, ciblant spécifiquement les environnements de développement (IDE). L'attaque utilise des extensions contrefaites pour compromettre l'intégralité des IDE présents sur une machine.

**Points clés :**
*   **Vecteur d'infection :** Une fausse extension Open VSX nommée `specstudio.code-wakatime-activity-tracker`, se faisant passer pour l'outil légitime WakaTime.
*   **Mécanisme d'exécution :** L'extension contient des binaires natifs (`win.node` ou `mac.node`) écrits en Zig. Ces fichiers s'exécutent hors de la sandbox JavaScript, permettant un accès complet au système.
*   **Propagation horizontale :** Le binaire détecte tous les IDE compatibles VS Code installés (VS Code, VSCodium, Cursor, Windsurf, etc.) et y installe silencieusement une seconde extension malveillante (`floktokbok.autoimport`), imitant l'extension populaire `autoimport`.
*   **Objectif final :** Le malware utilise la blockchain Solana pour localiser son serveur de commande et contrôle (C2), exfiltrer des données sensibles, déployer un RAT (Remote Access Trojan) et installer un infostealer pour Google Chrome.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car il s'agit d'une technique d'abus de fonctionnalités légitimes (*Supply Chain Attack* via des extensions tierces). La vulnérabilité réside dans l'exécution de code binaire non vérifié par les IDE avec des privilèges élevés.

**Recommandations :**
*   **Vérification immédiate :** Supprimer les extensions suspectes `specstudio.code-wakatime-activity-tracker` et `floktokbok.autoimport`.
*   **Rotation des secrets :** En cas d'installation confirmée, considérer le système comme totalement compromis. Procéder immédiatement à la rotation de tous les identifiants, jetons d'API, clés SSH et autres secrets stockés sur la machine.
*   **Prudence :** Installer uniquement des extensions provenant de sources vérifiées et inspecter les permissions demandées avant toute installation dans un environnement de développement.

---
[Source](https://thehackernews.com/2026/04/glassworm-campaign-uses-zig-dropper-to.html){:target="_blank"}
