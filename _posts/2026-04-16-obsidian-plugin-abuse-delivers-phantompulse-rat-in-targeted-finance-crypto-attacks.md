---
title: 'Obsidian Plugin Abuse Delivers PHANTOMPULSE RAT in Targeted Finance, Crypto Attacks'
date: 2026-04-16
permalink: /posts/2026/04/16/obsidian-plugin-abuse-delivers-phantompulse-rat-in-targeted-finance-crypto-attacks/
tags:
- veille-cyber
- hackernews
---
### Menace PHANTOMPULSE : Détournement d'Obsidian via Ingénierie Sociale

Une campagne d'ingénierie sociale sophistiquée (suivie sous l'identifiant **REF6598**) cible les professionnels de la finance et des cryptomonnaies en utilisant l'application de prise de notes **Obsidian** comme vecteur d'infection. Les attaquants incitent leurs victimes à synchroniser un "vault" (coffre-fort) cloud malveillant, permettant l'exécution arbitraire de code via des plugins légitimes détournés.

**Points clés :**
*   **Mode opératoire :** Prise de contact sur LinkedIn, migration vers Telegram pour instaurer un climat de confiance, puis demande d'accès à un dashboard partagé via Obsidian.
*   **Technique d'exécution :** L'attaque repose sur le détournement des plugins **"Shell Commands"** et **"Hider"**. Une fois la synchronisation des plugins communautaires activée par la victime (action manuelle requise), le fichier de configuration JSON déclenche le téléchargement de malwares.
*   **Payload PHANTOMPULSE :** Un RAT (Remote Access Trojan) généré par IA, capable de voler des données, capturer des frappes clavier, effectuer des captures d'écran et injecter des processus malveillants.
*   **C2 décentralisé :** Le malware utilise la blockchain Ethereum pour résoudre l'adresse de son serveur de commande et contrôle (C2), compliquant la détection et le blocage des infrastructures.
*   **Multi-plateforme :** L'attaque cible Windows (via un script PowerShell) et macOS (via AppleScript).

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique (type CVE), mais d'un **abus de fonctionnalités légitimes** (Community Plugins) et d'ingénierie sociale pour contourner les contrôles de sécurité.
*   Utilisation de la fonction **COM Elevation Moniker** pour l'élévation de privilèges sous Windows.

**Recommandations :**
*   **Vigilance accrue :** Ne jamais activer la synchronisation de plugins communautaires provenant de sources non fiables ou inconnues dans Obsidian.
*   **Gestion des permissions :** Maintenir les options de synchronisation des plugins désactivées par défaut et restreindre l'utilisation des plugins aux besoins strictement nécessaires.
*   **Surveillance comportementale :** Puisque l'exécution est portée par une application légitime et signée, les solutions EDR doivent se concentrer sur la détection des processus parents (ex: Obsidian lançant PowerShell ou des scripts suspects) plutôt que sur les signatures antivirus traditionnelles.
*   **Sensibilisation :** Former le personnel aux tactiques d'ingénierie sociale complexes impliquant des plateformes professionnelles et des groupes de messagerie privée.

---
[Source](https://thehackernews.com/2026/04/obsidian-plugin-abuse-delivers.html){:target="_blank"}
