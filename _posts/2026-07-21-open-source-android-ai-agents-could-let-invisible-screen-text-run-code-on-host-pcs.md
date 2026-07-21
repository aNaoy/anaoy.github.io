---
title: 'Open-Source Android AI Agents Could Let Invisible Screen Text Run Code on Host PCs'
date: 2026-07-21
permalink: /posts/2026/07/21/open-source-android-ai-agents-could-let-invisible-screen-text-run-code-on-host-pcs/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les frameworks d'agents IA pour Android

Des chercheurs ont mis en évidence sept vecteurs d'attaque ciblant cinq frameworks open-source d'agents mobiles (AppAgent, AppAgentX, Mobile-Agent-v3, Open-AutoGLM et MobA). Ces failles permettent à une application malveillante de prendre le contrôle de l'ordinateur hôte ou de dérober des données utilisateur en manipulant ce que l'IA "voit" à l'écran.

#### Points clés
*   **Injection de commandes hôte :** Les frameworks transmettent les sorties du modèle LLM directement à des commandes shell sans assainissement adéquat, permettant une exécution de code à distance (RCE) sur le PC contrôlant le téléphone.
*   **Manipulation de vision (Prompt Injection) :** Les modèles IA sont vulnérables à des textes invisibles (faible opacité) ou placés dans des zones masquées de l'écran, poussant l'agent à effectuer des actions malveillantes.
*   **Attaques par "File Race" :** Les agents capturent souvent des captures d'écran via des fichiers temporaires sur la carte SD. Une application malveillante peut remplacer ces fichiers en quelques millisecondes pendant le traitement de l'image.
*   **Absence d'authentification clavier :** Certains agents utilisent des outils comme "ADB Keyboard" qui acceptent des commandes broadcast sans authentification, permettant à n'importe quelle application d'injecter des entrées texte à la place de l'IA.
*   **Absence de réponse :** Les développeurs des frameworks concernés n'ont pas répondu aux signalements privés des chercheurs. Aucun CVE n'a été attribué à ce jour.

#### Vulnérabilités identifiées
*   **Injection shell :** Utilisation de `shell=True` dans les appels système avec des entrées non filtrées.
*   **TOCTOU (Time-of-Check to Time-of-Use) :** Course aux fichiers lors de la capture d'écran via `/sdcard`.
*   **UI Spoofing / Attaques par recouvrement :** Utilisation de fenêtres invisibles ou de services d'accessibilité pour masquer les intentions réelles de l'utilisateur.

#### Recommandations pour les développeurs
*   **Sécurisation des commandes :** Proscrire l'usage de `shell=True` et privilégier le passage d'arguments via des listes (argv) pour neutraliser les caractères spéciaux du shell.
*   **Streaming de données :** Privilégier le flux de données direct (ex: `exec-out`) pour les captures d'écran afin d'éviter le stockage temporaire sur le disque et les attaques par "File Race".
*   **Authentification et permissions :** Utiliser des permissions de niveau "signature" pour les broadcasts d'entrée de texte et restreindre les intents.
*   **Contexte et validation :** Implémenter une vérification du contexte avant chaque action et restreindre les domaines d'application à une liste blanche de paquets autorisés.
*   **Principe de prudence :** Garder à l'esprit que "le LLM n'est pas une limite de sécurité" ; les actions sensibles doivent toujours être confirmées par l'utilisateur via une interface dédiée.

---
[Source](https://thehackernews.com/2026/07/open-source-android-ai-agents-could-let.html){:target="_blank"}
