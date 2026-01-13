---
title: 'Malicious Chrome Extension Steals MEXC API Keys by Masquerading as Trading Tool'
date: 2026-01-13
permalink: /posts/2026/01/13/malicious-chrome-extension-steals-mexc-api-keys-by-masquerading-as-trading-tool/
tags:
- veille-cyber
- hackernews
---
## Extension Chrome Malveillante : Vol de Clés API MEXC

Une extension Google Chrome, nommée "MEXC API Automator", a été découverte dérobant les clés API de la plateforme d'échange de cryptomonnaies MEXC. Cette extension, téléchargeable sur le Chrome Web Store, se présente comme un outil d'automatisation de trading.

**Fonctionnement de l'attaque :**

Une fois installée et l'utilisateur naviguant sur la page de gestion des clés API de MEXC, l'extension injecte un script qui :
* Crée de nouvelles clés API MEXC.
* Active la permission de retrait.
* Dissimule cette activation dans l'interface utilisateur.
* Exfiltre la clé d'accès et le secret vers un bot Telegram contrôlé par l'attaquant via une requête HTTPS POST.

L'exploitation d'une session navigateur déjà authentifiée permet à l'extension de contourner les mécanismes de sécurité classiques.

**Points clés :**

*   **Cible :** Clés API MEXC, y compris les permissions de retrait.
*   **Méthode de distribution :** Chrome Web Store.
*   **Canal d'exfiltration :** Bot Telegram.
*   **Vulnérabilité exploitée :** Session navigateur authentifiée et flux de création/gestion des clés API.
*   **Impact :** Contrôle total du compte MEXC de la victime, permettant des transactions, des retraits et le drainage de fonds. Les clés compromises restent valides jusqu'à révocation.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. L'attaque repose sur l'exploitation de fonctionnalités légitimes et d'une session authentifiée.

**Recommandations :**

*   **Prudence avec les extensions :** Installer uniquement des extensions provenant de sources fiables et examiner attentivement leurs permissions.
*   **Surveillance des activités API :** Vérifier régulièrement les clés API générées sur MEXC et révoquer celles qui sont suspectes ou inutilisées.
*   **Restrictions des permissions :** Lors de la création de clés API, accorder uniquement les permissions strictement nécessaires (par exemple, désactiver les retraits si l'automatisation de trading n'en a pas besoin).
*   **Détection et suppression :** Les utilisateurs ayant installé l'extension devraient immédiatement vérifier leurs clés API MEXC et révoquer toute clé suspecte. L'extension devrait être désinstallée.
*   **Adaptabilité :** Les chercheurs soulignent que cette méthode peut être adaptée à d'autres plateformes d'échange, portefeuilles DeFi et consoles web émettant des jetons.

L'extension "MEXC API Automator" (ID: pppdfgkfdemgfknfnhpkibbkabhghhfh) était encore disponible sur le Chrome Web Store au moment de la publication de l'article.

---
[Source](https://thehackernews.com/2026/01/malicious-chrome-extension-steals-mexc.html){:target="_blank"}
