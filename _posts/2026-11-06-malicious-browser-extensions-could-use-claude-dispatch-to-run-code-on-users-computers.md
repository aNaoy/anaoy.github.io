---
title: 'Malicious Browser Extensions Could Use Claude Dispatch to Run Code on Users Computers'
date: 2026-11-06
permalink: /posts/2026/11/06/malicious-browser-extensions-could-use-claude-dispatch-to-run-code-on-users-computers/
tags:
- veille-cyber
- hackernews
---
### Risque d'exécution de code à distance via la fonctionnalité Dispatch de Claude

Des chercheurs de Forever Security ont mis en évidence une vulnérabilité critique permettant à des extensions de navigateur malveillantes d'exécuter des commandes arbitraires sur l'ordinateur d'un utilisateur via l'application « Claude Desktop ».

**Points clés :**
*   **Vecteur d'attaque :** La faille repose sur la fonctionnalité « Dispatch », qui autorise l'envoi de tâches depuis le site claude.ai vers l'application de bureau.
*   **Mécanisme :** Une extension malveillante injectée dans le navigateur peut simuler des interactions utilisateur, contourner les demandes d'autorisation de Claude et ordonner l'installation de paquets (ex: npm) ou l'accès à des fichiers locaux.
*   **Portée :** L'attaque peut compromettre non seulement la machine locale, mais aussi tout autre appareil connecté au même compte utilisateur via Dispatch.
*   **Statu quo :** Anthropic a prévu de retirer la fonctionnalité Dispatch, bien que des mécanismes similaires dans d'autres outils (Claude Code Remote Control, Claude Cowork) présentent des risques analogues selon les chercheurs.

**Vulnérabilités :**
*   Aucun identifiant CVE n'a été attribué. Le problème réside dans une faille de conception permettant à un script tiers d'interagir avec Claude Desktop sans authentification forte, en détournant la session active de l'utilisateur.

**Recommandations :**
*   **Désactivation :** Désactiver immédiatement la fonctionnalité « Dispatch » (et les fonctions de contrôle à distance) dans les paramètres de Claude Desktop si l'usage n'est pas strictement nécessaire.
*   **Gestion des extensions :** Appliquer une politique de moindre privilège aux extensions de navigateur. Désinstaller celles qui ne sont pas indispensables et surveiller leurs permissions d'accès aux sites.
*   **Vigilance comportementale :** Surveiller les actions des agents IA, notamment les tentatives d'installation de logiciels, les modifications de configuration ou les connexions réseau inhabituelles.

---
[Source](https://thehackernews.com/2026/11/malicious-browser-extensions-could-use.html){:target="_blank"}
