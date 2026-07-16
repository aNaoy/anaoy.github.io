---
title: 'New ClickLock macOS Stealer Kills Apps Every 210ms Until Victims Type Their Password'
date: 2026-07-16
permalink: /posts/2026/07/16/new-clicklock-macos-stealer-kills-apps-every-210ms-until-victims-type-their-password/
tags:
- veille-cyber
- hackernews
---
### ClickLock : Le malware macOS qui prend votre bureau en otage

Le malware **ClickLock** est un nouveau logiciel espion (*infostealer*) pour macOS utilisant la technique de « ClickFix ». Il force les victimes à fournir leur mot de passe administrateur en rendant le système inutilisable par une boucle de fermeture forcée d'applications (toutes les 210 millisecondes).

**Points clés :**
*   **Mode opératoire :** Le malware est déployé via une commande copiée-collée dans le terminal. Il affiche une fausse interface Cloudflare, puis utilise des boîtes de dialogue système falsifiées pour soutirer le mot de passe utilisateur.
*   **Persistance par coercition :** Si la victime refuse, le malware installe des *LaunchAgents* qui ferment en boucle le Finder, le Dock, les navigateurs et le moniteur d'activité. La machine devient inutilisable jusqu'à ce que l'utilisateur saisisse son mot de passe.
*   **Objectifs :** Une fois le mot de passe obtenu, le malware exfiltre le trousseau d'accès (Keychain), les mots de passe enregistrés, les cookies, les portefeuilles de cryptomonnaies et les historiques shell.
*   **Backdoor :** Il installe une porte dérobée persistante nommée « goyim » (basée sur GSocket), permettant un accès distant via un tunnel chiffré sans serveur C2 dédié.

**Vulnérabilités :**
Il n'existe pas de CVE spécifique, car le malware exploite le comportement légitime du système :
*   **Abus des `LaunchAgents` :** Permet la persistance des processus malveillants.
*   **Ingénierie sociale (ClickFix) :** Contourne les avertissements de sécurité Apple en convaincant l'utilisateur d'exécuter lui-même des commandes malveillantes.
*   **Accès complet au disque :** Le malware guide les victimes pour octroyer manuellement des permissions excessives.

**Recommandations :**
*   **Ne jamais coller de commandes inconnues** dans le Terminal, même si un site web le demande.
*   **Réaction en cas d'infection :** 
    *   Ne pas saisir son mot de passe. Éteindre brutalement la machine via le bouton d'alimentation.
    *   Démarrer en **Mode sans échec** (Shift au démarrage) pour supprimer les fichiers malveillants (`~/Library/LaunchAgents/` et `~/Library/Application Support/iCloudsync`).
    *   Changer immédiatement tous les mots de passe et révoquer les sessions actives (navigateurs, portefeuilles, services cloud).
*   **Vigilance :** Se méfier des processus suspects se faisant passer pour des services système (ex: `SystemUIServerl` avec un 'l' minuscule à la fin).

---
[Source](https://thehackernews.com/2026/07/new-clicklock-macos-stealer-kills-apps.html){:target="_blank"}
