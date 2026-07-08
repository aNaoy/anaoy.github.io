---
title: 'Court Filing Reveals Windows Device ID Helped FBI Trace Alleged Scattered Spider Hacker'
date: 2026-07-08
permalink: /posts/2026/07/08/court-filing-reveals-windows-device-id-helped-fbi-trace-alleged-scattered-spider-hacker/
tags:
- veille-cyber
- hackernews
---
### Identification d'un pirate par son identifiant unique Windows

**Points clés :**
*   **Mode opératoire :** Les attaquants du groupe "Scattered Spider" ont utilisé l'ingénierie sociale (appel au support IT en se faisant passer pour des employés) pour réinitialiser des mots de passe et des configurations MFA.
*   **Activités malveillantes :** Exfiltration de 77 Go de données via des outils de tunneling (ngrok, Teleport) et tentative de déploiement de ransomware.
*   **Preuve numérique :** L'enquête a abouti grâce au *Global Device Identifier* (GDI) de Microsoft, un identifiant matériel persistant associé à l'installation Windows du pirate, corrélé à ses comptes personnels et à ses déplacements géographiques.
*   **Structure du groupe :** Scattered Spider n'est pas une entité centralisée, mais un collectif de cellules indépendantes, rendant les arrestations individuelles peu efficaces pour neutraliser la menace globale.

**Vulnérabilités exploitées :**
*   Absence de processus de vérification rigoureux lors des appels au support technique (pas de CVE spécifique, faille humaine et procédurale).
*   Utilisation de méthodes d'authentification MFA vulnérables au "MFA fatigue" ou à la réinitialisation frauduleuse via le support client.

**Recommandations :**
*   **Sécurisation du support technique :** Instaurer des protocoles de vérification d'identité stricts avant toute réinitialisation (rappel sur numéro enregistré, validation par un manager ou vérification vidéo pour les accès privilégiés).
*   **Mise en place de MFA résistant au phishing :** Utiliser des clés de sécurité matérielles (type FIDO2) pour protéger les accès critiques.
*   **Monitoring des comportements :** Surveiller l'utilisation d'outils de tunneling (ngrok, Teleport) et les accès suspects vers des espaces de stockage cloud.
*   **Réduction de la surface d'attaque :** Limiter les privilèges administratifs et auditer régulièrement les accès aux systèmes de support IT.

---
[Source](https://thehackernews.com/2026/07/court-filing-reveals-windows-device-id.html){:target="_blank"}
