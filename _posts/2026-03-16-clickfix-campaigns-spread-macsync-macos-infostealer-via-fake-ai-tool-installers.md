---
title: 'ClickFix Campaigns Spread MacSync macOS Infostealer via Fake AI Tool Installers'
date: 2026-03-16
permalink: /posts/2026/03/16/clickfix-campaigns-spread-macsync-macos-infostealer-via-fake-ai-tool-installers/
tags:
- veille-cyber
- hackernews
---
### Expansion des campagnes « ClickFix » : Menace sur les utilisateurs macOS et Windows

Les campagnes « ClickFix » (ou « InstallFix ») connaissent une recrudescence majeure, exploitant l'ingénierie sociale pour inciter les utilisateurs à exécuter manuellement des commandes malveillantes dans leur terminal. Ces attaques, qui ciblent particulièrement les développeurs et les utilisateurs d'outils d'IA, permettent le déploiement de logiciels espions (infostealers).

**Points clés :**
*   **Mode opératoire :** Les attaquants utilisent le référencement payant (Google Ads) ou des sites compromis (notamment WordPress) pour rediriger les victimes vers de fausses pages de téléchargement ou de faux outils d'IA.
*   **Le leurre :** La victime est invitée à copier-coller une commande dans le Terminal (souvent sous couvert d'une installation logicielle légitime ou d'un test de sécurité « CAPTCHA »).
*   **Infection macOS :** Le logiciel malveillant **MacSync** récolte des identifiants, des clés SSH, des bases de données de trousseaux et des phrases de récupération de portefeuilles cryptographiques.
*   **Infection Windows :** Des logiciels comme **StealC**, **Vidar**, **Impure** ou **VodkaStealer** sont déployés via des droppers ou des extensions de navigateur malveillantes.

**Vulnérabilités exploitées :**
*   Bien qu'aucune CVE spécifique ne soit citée pour le mécanisme d'infection lui-même, les compromissions de sites WordPress exploitent généralement des **vulnérabilités non corrigées dans des thèmes ou extensions**, ainsi que des accès administrateur compromis (mots de passe faibles, absence de MFA).

**Recommandations :**
*   **Pour les utilisateurs :** Ne jamais copier-coller des commandes provenant d'un site web dans votre terminal, même si le site semble légitime ou officiel. Maintenir une approche « Zero Trust » face aux outils téléchargés.
*   **Pour les administrateurs de sites (WordPress) :**
    *   Maintenir les CMS, thèmes et extensions à jour.
    *   Utiliser des mots de passe robustes et activer l'authentification à deux facteurs (2FA) pour tous les accès administrateur.
    *   Auditer régulièrement la liste des comptes administrateurs à la recherche d'accès suspects.
    *   Utiliser des logiciels de sécurité réputés pour détecter les injections malveillantes.

---
[Source](https://thehackernews.com/2026/03/clickfix-campaigns-spread-macsync-macos.html){:target="_blank"}
