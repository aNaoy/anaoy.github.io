---
title: 'A Shared ChatGPT Link Could Run Attacker Code in Your Session and Read Private Chats'
date: 2026-10-31
permalink: /posts/2026/10/31/a-shared-chatgpt-link-could-run-attacker-code-in-your-session-and-read-private-chats/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans ChatGPT : Risque d'exécution de code à distance via des liens partagés

Des chercheurs de la société Parameter ont identifié une faille de sécurité majeure (classée P1 par OpenAI) permettant à un attaquant d'exécuter du code arbitraire au sein de la session active d'un utilisateur de ChatGPT. En ouvrant un lien de conversation malveillant, une victime pouvait voir ses discussions privées compromises et son compte utilisé pour effectuer des actions non autorisées.

**Points clés :**
*   **Vecteur d'attaque :** Un simple lien de partage ChatGPT, diffusé via e-mail, réseaux sociaux ou messagerie. Aucune installation n'était requise, l'attaque se déclenchait lors de l'affichage d'un aperçu (Preview).
*   **Impact :** Accès complet aux API de la victime, lecture des conversations privées et possibilité d'agir pour le compte de l'utilisateur.
*   **Mécanisme :** L'attaque exploitait une mauvaise gestion de la communication entre les cadres (frames) du navigateur. Une bibliothèque mathématique (MathLive) acceptait des messages contenant du code HTML non vérifié provenant d'une source non sécurisée, permettant de briser le "bac à sable" (sandbox) de la fonctionnalité *Preview* et d'injecter du code dans la page principale de ChatGPT.

**Vulnérabilités :**
*   Absence de validation de l'origine des messages inter-cadres (postMessage).
*   Autorisation de contenu HTML arbitraire dans les paramètres de configuration d'un composant tiers.
*   Héritage inapproprié des permissions du domaine `chatgpt.com` par un cadre injecté.
*   *Note : Aucune référence CVE spécifique n'est mentionnée pour cette correction traitée via le programme de bug bounty d'OpenAI.*

**Recommandations :**
*   **Pour les utilisateurs :** Aucune action requise. OpenAI a déployé une correction côté serveur le 26 octobre 2024.
*   **Pour les développeurs :** L'incident souligne l'importance critique de valider systématiquement l'origine des messages `postMessage` dans les architectures utilisant des *iframes* et de restreindre strictement les politiques de sécurité de contenu (CSP), même pour les ressources provenant de domaines tiers autorisés.

---
[Source](https://thehackernews.com/2026/10/a-shared-chatgpt-link-could-run.html){:target="_blank"}
