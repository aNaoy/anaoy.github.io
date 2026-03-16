---
title: 'DRILLAPP Backdoor Targets Ukraine, Abuses Microsoft Edge Debugging for Stealth Espionage'
date: 2026-03-16
permalink: /posts/2026/03/16/drillapp-backdoor-targets-ukraine-abuses-microsoft-edge-debugging-for-stealth-espionage/
tags:
- veille-cyber
- hackernews
---
### DRILLAPP : Espionnage furtif via détournement du navigateur Edge

Une nouvelle campagne de cyberespionnage, liée au groupe Laundry Bear (UAC-0190), cible des entités ukrainiennes en utilisant un backdoor JavaScript baptisé **DRILLAPP**. Ce malware exploite les fonctionnalités de débogage de Microsoft Edge pour mener des activités malveillantes sous couvert d'un processus légitime.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de fichiers LNK ou de modules du Panneau de configuration Windows pour lancer des scripts malveillants hébergés sur Pastefy.
*   **Technique d'évasion :** Le malware exécute Microsoft Edge en mode « headless » avec des paramètres de sécurité désactivés (ex: `--no-sandbox`, `--disable-web-security`).
*   **Fonctionnalités :** Accès au système de fichiers, capture d'écran, enregistrement audio/vidéo et identification des victimes par empreinte numérique (canvas fingerprinting).
*   **Détournement :** Utilisation du protocole *Chrome DevTools Protocol* (CDP) pour contourner les restrictions natives de JavaScript sur le téléchargement de fichiers.

**Vulnérabilités :**
L'attaque ne repose pas sur une CVE spécifique, mais sur l'abus de fonctionnalités légitimes de Chromium (« design-by-feature »). L'utilisation de paramètres de débogage (`--remote-debugging-port`) permet de transformer un navigateur standard en outil d'espionnage capable de passer outre les contrôles de sécurité.

**Recommandations :**
*   **Surveillance des processus :** Auditer les lignes de commande des navigateurs. Toute exécution d'un navigateur avec des drapeaux de sécurité désactivés (`--no-sandbox`, `--disable-web-security`, etc.) doit être bloquée et alertée immédiatement.
*   **Contrôle des fichiers de démarrage :** Surveiller étroitement le dossier de démarrage (Startup) de Windows pour détecter la création de raccourcis suspects.
*   **Politiques de sécurité (GPO) :** Restreindre l'exécution de fichiers HTA et limiter l'utilisation des fonctionnalités de débogage à distance sur les postes des utilisateurs finaux.
*   **Analyse comportementale :** Privilégier les solutions EDR capables d'identifier les comportements suspects initiés par des navigateurs (ex: accès anormal à la caméra ou au microphone).

---
[Source](https://thehackernews.com/2026/03/drillapp-backdoor-targets-ukraine.html){:target="_blank"}
