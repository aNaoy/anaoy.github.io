---
title: 'Apple Screen Sharing Security, (Mon, Aug 17th)'
date: 2026-08-17
permalink: /posts/2026/08/17/apple-screen-sharing-security-mon-aug-17th/
tags:
- veille-cyber
- sans-isc
---
### Vulnérabilités et sécurisation du partage d'écran macOS

Le partage d'écran d'Apple repose sur le protocole VNC, une technologie historiquement non chiffrée utilisant le port TCP 5900. Des modifications propriétaires apportées par Apple à ce protocole ont récemment engendré des vulnérabilités critiques actuellement exploitées, rendant tout système exposé potentiellement compromis.

**Points clés**
*   **Dualité d'authentification :** Apple supporte à la fois l'authentification VNC classique (basée uniquement sur un mot de passe global) et le système d'authentification macOS. La méthode classique est particulièrement vulnérable car elle contourne les contrôles d'accès stricts.
*   **Insuffisance du pare-feu :** L'activation du pare-feu macOS ne suffit pas à bloquer le partage d'écran si les options « autoriser automatiquement les logiciels intégrés » ou « logiciels signés » sont activées.
*   **Risque d'élévation :** L'accès via VNC s'exécute avec des privilèges élevés, facilitant l'exploitation si l'authentification est faible.

**Recommandations de sécurité**
*   **Restreindre les accès :** Limiter strictement les utilisateurs autorisés à se connecter à distance.
*   **Utiliser un tunnel sécurisé :** Ne jamais exposer directement le port 5900 sur Internet. Privilégier systématiquement un tunnel VPN, le transfert SSH (SSH forwarding) ou des solutions comme Tailscale.
*   **Durcissement via ligne de commande :**
    *   Activer le pare-feu et le mode furtif (*stealth mode*).
    *   Désactiver l'autorisation automatique des logiciels signés (`--setallowsigned off`).
    *   Désactiver les services de partage d'écran (`com.apple.screensharing`) et de fichiers (`com.apple.smbd`) lorsqu'ils ne sont pas nécessaires, particulièrement sur les réseaux publics.
*   **Audit :** Vérifier régulièrement l'état du pare-feu via `/usr/libexec/ApplicationFirewall/socketfilterfw --getglobalstate`.

---
[Source](https://isc.sans.edu/diary/rss/33252){:target="_blank"}
