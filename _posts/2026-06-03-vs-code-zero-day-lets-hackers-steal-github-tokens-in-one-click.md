---
title: 'VS Code zero-day lets hackers steal GitHub tokens in one click'
date: 2026-06-03
permalink: /posts/2026/06/03/vs-code-zero-day-lets-hackers-steal-github-tokens-in-one-click/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité zero-day dans VS Code : vol de jetons GitHub

Une faille de sécurité critique a été découverte dans Visual Studio Code (VS Code), permettant à un attaquant de dérober les jetons d'authentification GitHub d'un utilisateur via une simple interaction (clic sur un lien). Cette vulnérabilité, actuellement non corrigée, exploite le système de messagerie « webview » de VS Code pour installer des extensions malveillantes.

**Points clés :**
*   **Mécanisme d'attaque :** L'exploitation repose sur l'envoi de jetons OAuth vers `github.dev`. Un attaquant utilise du JavaScript malveillant dans une webview pour simuler des actions utilisateur, installer une extension et extraire le jeton.
*   **Impact :** Une fois le jeton compromis, l'attaquant accède à l'intégralité des dépôts GitHub de la victime, y compris les dépôts privés, car le jeton n'est pas restreint au seul dépôt consulté.
*   **Contexte de divulgation :** Le chercheur Ammar Askar a procédé à une divulgation publique immédiate, critiquant la gestion passée des rapports de vulnérabilités par le Microsoft Security Response Center (MSRC).

**Vulnérabilités :**
*   **Identifiant CVE :** Aucun identifiant n'a été attribué à ce jour.

**Recommandations :**
*   **Atténuation immédiate :** Les utilisateurs sont invités à supprimer les cookies et les données de site locale pour `github.dev` dans leur navigateur. 
    *   *Procédure :* Cliquer sur l'icône des paramètres dans la barre d'URL > Cookies et données de site > Gérer les données de site.
*   **Résultat attendu :** Cette opération force VS Code à afficher à nouveau la fenêtre de consentement (« The extension 'GitHub Repositories' wants to sign in using GitHub »), permettant à l'utilisateur de valider explicitement l'accès.

---
[Source](https://www.bleepingcomputer.com/news/security/vs-code-zero-day-lets-hackers-steal-github-tokens-in-one-click/){:target="_blank"}
