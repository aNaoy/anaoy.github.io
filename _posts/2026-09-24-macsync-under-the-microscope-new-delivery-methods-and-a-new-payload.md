---
title: 'MacSync under the microscope: new delivery methods and a new payload'
date: 2026-09-24
permalink: /posts/2026/09/24/macsync-under-the-microscope-new-delivery-methods-and-a-new-payload/
tags:
- veille-cyber
- securelist
---
### Évolution de MacSync : Analyse d'une nouvelle chaîne d'infection macOS

MacSync est un infostealer en pleine mutation, passant de scripts AppleScript rudimentaires à des binaires complexes en Swift et Objective-C. Distribué via le modèle Malware-as-a-Service (MaaS), il se fait passer pour des applications légitimes (ex: portefeuille crypto "Toria") pour cibler principalement les développeurs et les passionnés de cryptomonnaies.

**Points clés :**
*   **Chaîne d'infection sophistiquée :** Abandon des droppers scriptés au profit de binaires (format FAT Mach-O) utilisant des techniques avancées (anti-VM, anti-débogage via `ptrace`).
*   **Infrastructure détournée :** Utilisation ponctuelle d'iCloud (calendriers publics) pour acheminer des commandes malveillantes.
*   **Persistance multi-niveaux :** Injection dans `.ZSHRC`, utilisation de `LaunchAgents` et hooks Git pour assurer la résilience du backdoor.
*   **Chiffrement de nouvelle génération :** Mise en œuvre d'un utilitaire personnalisé (`pkgunpack`) utilisant l'échange de clés ECDH sur Curve25519 et le chiffrement AES-GCM pour protéger les modules téléchargés.
*   **Technique PAM :** Adoption de l'API *Pluggable Authentication Modules* pour usurper l'authentification administrateur, une méthode rare sur macOS.

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur le **"Social Engineering"** (téléchargement d'applications compromises) et le détournement de fonctionnalités légitimes du système (LaunchAgents, hooks Git, API PAM) pour contourner les protections macOS.

**Recommandations :**
*   **Vigilance sur l'origine des logiciels :** Éviter les applications "crackées" ou les portefeuilles crypto non vérifiés promus via les réseaux sociaux (X, Telegram).
*   **Contrôle des privilèges :** Se méfier des fenêtres contextuelles système demandant des mots de passe administrateur après l'ouverture d'une application nouvellement téléchargée.
*   **Audit de configuration :** Surveiller les fichiers de configuration des interpréteurs (`.ZSHRC`, `.bash_profile`) et les hooks Git pour détecter toute commande suspecte ou persistante.
*   **Sécurité des accès :** Protéger le trousseau d'accès (Keychain) et limiter l'accès aux secrets pour les applications non signées par des développeurs identifiés.
*   **Utilisation de solutions de sécurité :** Déployer des outils capables de détecter les comportements suspects liés aux verdicts `HEUR:Trojan.OSX.MacSync.*`.

---
[Source](https://securelist.com/macsync-new-version/121383/){:target="_blank"}
