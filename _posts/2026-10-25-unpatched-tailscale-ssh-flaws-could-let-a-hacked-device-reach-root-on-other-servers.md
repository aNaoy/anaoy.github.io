---
title: 'Unpatched Tailscale SSH Flaws Could Let a Hacked Device Reach Root on Other Servers'
date: 2026-10-25
permalink: /posts/2026/10/25/unpatched-tailscale-ssh-flaws-could-let-a-hacked-device-reach-root-on-other-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Tailscale SSH : Risque d'élévation de privilèges

Des failles de sécurité, documentées dans le rapport « Tailworm » par Erica Windisch, exposent les utilisateurs de Tailscale à un risque d'élévation de privilèges vers le compte `root`. Ces vulnérabilités, bien que non encore officiellement classées par un identifiant CVE et sans correctif disponible à ce jour, permettent à un attaquant ayant déjà compromis un appareil sur le réseau d'accéder aux autres serveurs autorisés avec des privilèges administrateur.

**Points clés :**
*   **Mécanisme :** L'attaque exploite la fonction de transfert de port (port forwarding) de Tailscale SSH. En manipulant des sockets Unix ou en exploitant des conditions de course (*race conditions*), un attaquant peut exécuter des commandes `root` sans authentification supplémentaire.
*   **Potentiel "Wormable" :** En laboratoire, une compromission initiale peut se propager automatiquement à l'ensemble du parc de machines autorisé, contournant les protections habituelles.
*   **Contexte :** Le risque concerne principalement les versions 1.104.2 (Tailscale) et 0.29.5 (Headscale). La fonctionnalité d'« app connector » présente également des risques de fuite de métadonnées cloud.

**Recommandations immédiates :**
*   **Durcir les règles d'accès :** Restreindre les politiques SSH à des paires source-destination spécifiques (un appareil vers un seul serveur) et éviter les règles globales basées sur des tags ou des identités.
*   **Désactiver le transfert de port :** Désactiver systématiquement le transfert de port SSH dans les paramètres de règles. Pour les utilisateurs de Headscale, considérer tout accès SSH comme une compromission totale du système cible.
*   **Sécurisation supplémentaire :** 
    *   Activer la fonctionnalité `Tailnet Lock`.
    *   Activer l'expiration des clés de nœud (*node-key expiry*).
    *   Supprimer les permissions d'app connector non essentielles et les redirections vers des sockets Unix (`tailscale serve`).
*   **Gestion des incidents :** En cas de compromission, supprimer immédiatement l'appareil du panneau de contrôle pour révoquer ses clés, car une simple réinstallation du système est insuffisante.

---
[Source](https://thehackernews.com/2026/10/unpatched-tailscale-ssh-flaws-could-let.html){:target="_blank"}
