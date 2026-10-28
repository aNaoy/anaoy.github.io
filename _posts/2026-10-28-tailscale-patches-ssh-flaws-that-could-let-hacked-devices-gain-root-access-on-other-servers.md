---
title: 'Tailscale Patches SSH Flaws That Could Let Hacked Devices Gain Root Access on Other Servers'
date: 2026-10-28
permalink: /posts/2026/10/28/tailscale-patches-ssh-flaws-that-could-let-hacked-devices-gain-root-access-on-other-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Tailscale SSH : Risques d'élévation de privilèges

Tailscale a corrigé plusieurs vulnérabilités majeures dans son service SSH intégré, identifiées sous le nom de code « Tailworm ». Ces failles permettent à un attaquant, déjà présent sur un appareil autorisé par la politique réseau, d'accéder à des services sensibles (comme le socket Docker ou l'API locale `tailscaled`) avec des privilèges root, alors que cela devrait être restreint.

**Points clés :**
*   **Mécanisme d'attaque :** L'exploitation repose sur une technique de « socket-swapping » exploitant une condition de course (race condition) lors du transfert de connexions. Le processus Tailscale, s'exécutant avec les privilèges root, peut être manipulé pour accéder à des fichiers ou services réservés au superutilisateur.
*   **Portée :** Les failles affectent les environnements Linux et macOS. Elles ne permettent pas une intrusion initiale sans authentification, mais facilitent un mouvement latéral rapide et l'élévation de privilèges sur les machines déjà cibles d'une règle SSH autorisée.
*   **Absence de CVE :** Au moment de la publication, aucun identifiant CVE n'a été attribué aux quatre bulletins de sécurité émis (TS-2026-014 à TS-2026-017).
*   **Spécificité Headscale :** Le serveur de contrôle auto-hébergé *Headscale* est particulièrement vulnérable car il ne permet pas de désactiver le transfert SSH par politique ; chaque session SSH doit donc être considérée comme ayant potentiellement les droits root.

**Vulnérabilités identifiées (Bulletins de sécurité) :**
*   **TS-2026-014 :** Failles de transfert de socket permettant l'accès à des services root-only.
*   **TS-2026-015 :** Risque de déni de service (DoS) par épuisement mémoire provoquant le plantage du processus.
*   **TS-2026-016 :** Problèmes dans `tailscale serve` permettant un contrôle distant via l'API locale.
*   **TS-2026-017 :** Fuite de permissions entre différents montages lors de l'utilisation de `TLS serve`.

**Recommandations :**
1.  **Mise à jour immédiate :** Passer à la version **1.104.4** ou supérieure.
2.  **Mesure d'atténuation temporaire :** Si la mise à jour est impossible, désactiver le transfert SSH en définissant la variable d'environnement `TS_SSH_DISABLE_FORWARDING=1` dans le service `tailscaled`.
3.  **Durcissement des politiques :** Restreindre les règles d'accès SSH au strict nécessaire (paires appareil-à-appareil) et utiliser le « check mode » (ré-authentification) pour les systèmes sensibles.
4.  **Gestion des clés :** En cas de compromission suspectée, supprimer et révoquer les clés d'appareil au niveau du plan de contrôle, car la simple réinstallation de la machine ne suffit pas à invalider les clés existantes.

---
[Source](https://thehackernews.com/2026/10/tailscale-patches-ssh-flaws-that-could.html){:target="_blank"}
