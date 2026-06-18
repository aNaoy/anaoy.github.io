---
title: 'ThreatsDay Bulletin: Claude Chat Abuse, NastyC2 npm Packages, Device-Code Phishing + 25 More Stories'
date: 2026-06-18
permalink: /posts/2026/06/18/threatsday-bulletin-claude-chat-abuse-nastyc2-npm-packages-device-code-phishing-25-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : L'exploitation de la confiance comme vecteur d'attaque

Le paysage actuel de la cybersécurité montre une tendance marquée où les attaquants détournent des outils et services légitimes pour faciliter des campagnes malveillantes. La confiance accordée aux plateformes (IA, extensions, gestionnaires de paquets) constitue désormais la principale surface d'attaque.

#### Points clés et menaces émergentes
*   **Détournement d'IA et d'agents :** Abus des fonctionnalités de partage de conversations Claude pour diffuser des malwares (MacSync) et vulnérabilités dans l'extension VS Code *Cline*, permettant une exécution de code arbitraire malgré les garde-fous.
*   **Attaques sur la chaîne d'approvisionnement :** Utilisation de paquets npm malveillants (*NastyC2*, *crypto-javascript*) pour déployer des frameworks post-exploitation, des mineurs de cryptomonnaie et des exploits de privilèges (Dirty Frag).
*   **Techniques sans fichier (Fileless) :** Multiplication des attaques macOS (ClickFix) et des chargeurs (OnionDrop) utilisant la mémoire vive pour éviter toute détection sur disque.
*   **Phishing et ingénierie sociale :** Campagnes ciblées sur WhatsApp pour des fraudes aux réservations hôtelières et abus du flux OAuth 2.0 (Device Code Phishing) pour détourner des comptes Microsoft 365.
*   **Reconnaissance HTTP/2 :** Exploitation de la vulnérabilité **CVE-2026-49975** (HTTP/2 Bomb) pour saturer la mémoire des serveurs via une amplification du trafic.

#### Vulnérabilités majeures
*   **CVE-2026-20127 :** Élévation de privilèges critique dans Cisco Catalyst SD-WAN (Controller, Manager, Validator). Permet un accès administrateur sans authentification.
*   **CVE-2026-49975 :** Attaque par épuisement de mémoire (DoS) sur les serveurs Apache HTTP via le protocole HTTP/2.

#### Recommandations stratégiques
*   **Audit des agents et outils :** Traiter les agents IA, les extensions de navigateur et les outils de développement avec la même méfiance que les exécutables non signés. Ne pas présumer de la sécurité d'un lien simplement parce qu'il provient d'une plateforme réputée.
*   **Gestion des correctifs :** Aligner les politiques de mise à jour sur la directive **BOD 26-04** de la CISA, en priorisant la remédiation sous 3 jours pour les vulnérabilités exploitées activement (KEV) sur les actifs exposés à Internet.
*   **Anticipation quantique :** Préparer la transition vers une cryptographie résistante aux futurs ordinateurs quantiques, conformément aux nouvelles exigences de l'ANSSI.
*   **Validation des logs :** Surveiller les incohérences dans les télémétries cloud (ex: écarts de données dans les logs GCP) qui pourraient masquer des activités malveillantes.

---
[Source](https://thehackernews.com/2026/06/threatsday-bulletin-claude-chat-abuse.html){:target="_blank"}
