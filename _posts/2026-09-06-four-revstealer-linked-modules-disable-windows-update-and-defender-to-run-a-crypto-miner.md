---
title: 'Four REVSTEALER-Linked Modules Disable Windows Update and Defender to Run a Crypto Miner'
date: 2026-09-06
permalink: /posts/2026/09/06/four-revstealer-linked-modules-disable-windows-update-and-defender-to-run-a-crypto-miner/
tags:
- veille-cyber
- hackernews
---
### REVSTEALER : Une menace persistante par modules malveillants

REVSTEALER est un "infostealer" commercial capable de dérober des identifiants de navigateurs, des portefeuilles de cryptomonnaies, des données de messagerie et des sessions de jeux vidéo. Bien que le logiciel principal se supprime après exfiltration pour effacer ses traces, il déploie quatre modules persistants (ProManager, WinUpdate, SoftManager et LockAppHost) qui s'installent durablement sur la machine de la victime.

**Points clés :**
*   **Propagation :** Principalement via des outils de triche pour jeux vidéo (YouTube) et des logiciels piratés ou contrefaits (ex: faux outils d'IA).
*   **Techniques de dissimulation :** Utilisation de contrats intelligents sur la blockchain Polygon pour récupérer des serveurs de commande (C2) de secours (technique "EtherHiding") et contournement des protections par des appels système indirects.
*   **Modules persistants :**
    *   **ProManager :** Superpose de fausses interfaces sur les portefeuilles crypto et enregistre la saisie au clavier.
    *   **WinUpdate :** Détourne le presse-papiers pour substituer des adresses de portefeuilles crypto.
    *   **SoftManager :** Transforme l'hôte infecté en proxy réseau inversé.
    *   **LockAppHost :** Désactive Windows Update et Microsoft Defender pour exécuter un mineur de cryptomonnaie en arrière-plan.

**Vulnérabilités et techniques exploitées :**
*   **Abus de CMSTP :** Utilisation de l'outil Windows *Connection Manager Profile Installer* pour obtenir des privilèges administrateur (sans CVE spécifique, technique classique d'élévation).
*   **App-Bound Encryption :** Extraction des clés de déchiffrement de Google Chrome en lançant le navigateur dans un débogueur pour lire la mémoire.

**Recommandations :**
*   **Remédiation post-infection :** Si le module *LockAppHost* a été détecté, il est impératif de réactiver manuellement les services Windows Update et les tâches planifiées, de supprimer les exclusions créées dans Microsoft Defender et de traquer tout mineur caché dans des processus système (ex: `svchost.exe`, `nslookup.exe`).
*   **Sécurité des comptes :** En raison du vol de cookies de session et de clés de chiffrement Chrome, un simple changement de mot de passe est insuffisant ; il est nécessaire d'invalider toutes les sessions actives sur les services compromis.
*   **Prévention :** Éviter impérativement le téléchargement de logiciels "gratuits" ou non officiels, notamment pour les outils d'IA ou les cheats de jeux. Utiliser uniquement les sources officielles des éditeurs.

---
[Source](https://thehackernews.com/2026/09/four-revstealer-linked-modules-disable.html){:target="_blank"}
