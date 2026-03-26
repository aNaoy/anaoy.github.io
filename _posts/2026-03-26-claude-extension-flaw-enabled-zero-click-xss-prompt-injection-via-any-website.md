---
title: 'Claude Extension Flaw Enabled Zero-Click XSS Prompt Injection via Any Website'
date: 2026-03-26
permalink: /posts/2026/03/26/claude-extension-flaw-enabled-zero-click-xss-prompt-injection-via-any-website/
tags:
- veille-cyber
- hackernews
---
### ShadowPrompt : Vulnérabilité critique dans l'extension Claude

Une faille de sécurité baptisée **ShadowPrompt** a été identifiée dans l'extension Google Chrome d'Anthropic (Claude). Cette vulnérabilité permettait à n'importe quel site web malveillant d'injecter des prompts de manière invisible dans l'assistant, sans interaction de l'utilisateur (zero-click), en usurpant l'identité de ce dernier.

**Points clés :**
*   **Mécanisme d'attaque :** Un attaquant utilise une iframe masquée sur son site web pour exploiter une faille XSS, permettant de communiquer avec l'extension via `postMessage`.
*   **Impact :** Vol de données sensibles, accès à l'historique des conversations, et exécution d'actions malveillantes (envoi d'emails ou extraction d'informations confidentielles) au nom de l'utilisateur.
*   **Chaînage des vulnérabilités :**
    *   **Permissivité excessive :** L'extension utilisait une liste blanche basée sur un pattern (`*.claude.ai`) trop large, autorisant n'importe quel sous-domaine à envoyer des commandes.
    *   **XSS (DOM-based) :** Présente dans un composant CAPTCHA d'Arkose Labs hébergé sur `a-cdn.claude.ai`.

**CVE :** Aucune CVE n'est mentionnée dans le rapport initial.

**Recommandations :**
*   **Mise à jour :** Assurez-vous que l'extension Claude Chrome est à jour (version 1.0.41 ou ultérieure), intégrant désormais une vérification stricte de l'origine exacte du domaine (`claude.ai`).
*   **Principe de moindre privilège :** Les développeurs d'extensions doivent restreindre strictement les communications inter-domaines et éviter les patterns génériques pour les listes blanches d'origines.
*   **Sécurisation tierce :** Il est crucial de surveiller la sécurité des composants tiers (comme les CAPTCHAs) intégrés au sein des applications, car ils constituent des vecteurs d'entrée potentiels.

---
[Source](https://thehackernews.com/2026/03/claude-extension-flaw-enabled-zero.html){:target="_blank"}
