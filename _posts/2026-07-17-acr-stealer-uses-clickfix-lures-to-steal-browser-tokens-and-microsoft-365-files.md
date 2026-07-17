---
title: 'ACR Stealer Uses ClickFix Lures to Steal Browser Tokens and Microsoft 365 Files'
date: 2026-07-17
permalink: /posts/2026/07/17/acr-stealer-uses-clickfix-lures-to-steal-browser-tokens-and-microsoft-365-files/
tags:
- veille-cyber
- hackernews
---
### Menace d'ACR Stealer : L'ingénierie sociale par "ClickFix"

**Points clés**
Le logiciel malveillant **ACR Stealer** (également associé à Amatera Stealer) exploite des techniques d'ingénierie sociale pour dérober des mots de passe enregistrés, des jetons de session actifs et des documents sensibles (Microsoft 365, PDF, OneDrive). Cette menace ne repose pas sur une vulnérabilité logicielle, mais sur la manipulation humaine : les victimes sont incitées à copier et exécuter manuellement une commande malveillante dans la boîte de dialogue « Exécuter » de Windows.

**Mécanismes d'infection**
*   **Technique « ClickFix » :** Utilisation de fausses pages (souvent liées à des publicités malveillantes ou du SEO manipulé, comme de faux outils d'IA) demandant à l'utilisateur de résoudre une erreur en collant un script.
*   **Chaîne de fichiers (Fileless) :** Utilisation de `mshta.exe` pour exécuter un script VBScript, lequel récupère une charge utile cachée dans les pixels d'une image JPEG (stéganographie) pour une exécution en mémoire.
*   **Chaîne persistante :** Chargement d'une DLL via un partage WebDAV distant, installation de scripts Python dissimulés et persistance via des tâches planifiées masquées sous forme de mises à jour logicielles.
*   **EtherHiding :** Utilisation de smart contracts sur la blockchain pour masquer les adresses des serveurs de commande et de contrôle (C2).

**Vulnérabilités**
*   **Aucune CVE identifiée :** L'attaque repose sur l'abus de fonctionnalités légitimes du système (PowerShell, `mshta.exe`, `rundll32.exe`) autorisées par l'utilisateur.

**Recommandations de sécurité**
*   **Durcissement du système :** Désactiver la boîte de dialogue « Exécuter » via GPO et restreindre l'utilisation de `mshta.exe` via AppLocker ou WDAC.
*   **Contrôle des applications :** Configurer des règles ASR (Attack Surface Reduction) pour empêcher PowerShell, Python et `rundll32.exe` de lancer des contenus provenant d'internet ou de répertoires temporaires/utilisateurs.
*   **Surveillance et détection :** Traquer l'exécution de `rundll32.exe` avec des connexions réseau suspectes, le « timestomping » (usurpation d'horodatage) et les effacements d'historique PowerShell.
*   **Réponse sur incident :** En cas d'infection, ne pas se limiter à une réinitialisation des mots de passe ; il est impératif de **révoquer tous les jetons de session (tokens)** pour invalider l'accès aux comptes compromis.

---
[Source](https://thehackernews.com/2026/07/acr-stealer-uses-clickfix-lures-to.html){:target="_blank"}
