---
title: 'Researchers Turn USB Auto-Install Into a Full SYSTEM Takeover on Windows 11'
date: 2026-08-11
permalink: /posts/2026/08/11/researchers-turn-usb-auto-install-into-a-full-system-takeover-on-windows-11/
tags:
- veille-cyber
- hackernews
---
### Plug and Pwn : Exploitation de l'installation automatique PnP sur Windows 11

Des chercheurs ont démontré qu'il est possible d'obtenir des privilèges **SYSTEM** sur Windows 11 en exploitant le mécanisme *Plug and Play* (PnP) lors de l'installation automatique de pilotes de périphériques USB. Cette technique permet de détourner des paquets de pilotes légitimes signés par des constructeurs pour exécuter du code malveillant.

**Points clés :**
*   **Vecteur physique :** Utilisation d'un appareil USB émulé pour déclencher l'installation automatique de pilotes vulnérables (Sierra Wireless, Sony FeliCa).
*   **Vecteur distant :** La même attaque est réalisable via le protocole RDP si la redirection USB de bas niveau est activée (configuration non activée par défaut).
*   **Mécanisme :** Enchaînement de failles incluant le détournement de l'ordre de recherche DLL (*DLL Hijacking*) et des vulnérabilités de traversée de chemin (*path traversal*) dans les composants d'installation des constructeurs.

**Vulnérabilités :**
*   Aucun identifiant CVE spécifique n'a été attribué à ce stade, car l'exploitation repose sur le détournement de processus d'installation légitimes et de faiblesses dans des paquets tiers (Sierra, Sony, Intel).

**Recommandations :**
*   **Restreindre l'installation des appareils :** Appliquer les stratégies de groupe (GPO) Microsoft pour bloquer l'installation de périphériques non autorisés via leurs identifiants matériels (*Hardware IDs*) ou classes d'installation.
*   **Sécuriser le protocole RDP :** S'assurer que la redirection USB de bas niveau et la redirection PnP sont désactivées sur les serveurs de bureau à distance, car elles ne sont pas nécessaires à la majorité des utilisateurs.
*   **Vigilance physique :** Limiter l'accès aux ports USB physiques sur les postes sensibles pour prévenir l'insertion de périphériques émulés malveillants.

---
[Source](https://thehackernews.com/2026/08/researchers-turn-usb-auto-install-into.html){:target="_blank"}
