---
title: 'Iran-Aligned Volant Manticore Uses IPFS-Based KuboShell Backdoor in Espionage Campaigns'
date: 2026-11-24
permalink: /posts/2026/11/24/iran-aligned-volant-manticore-uses-ipfs-based-kuboshell-backdoor-in-espionage-campaigns/
tags:
- veille-cyber
- hackernews
---
### Volant Manticore : Une nouvelle menace liée à l'Iran utilisant IPFS

Le groupe **Volant Manticore**, une entité probablement issue d'anciens opérateurs de MuddyWater et affiliée au ministère iranien du Renseignement (MOIS), mène des campagnes d'espionnage informatique depuis août 2025. Le groupe se distingue par des objectifs stratégiques évolutifs, ciblant des infrastructures critiques, les secteurs de la santé et les transports (aérien) à Chypre et en Arabie saoudite.

#### Points clés
*   **Mode opératoire :** Utilisation de campagnes de phishing basées sur des CV générés par IA ou des thématiques de séminaires de santé pour diffuser des malwares.
*   **Infrastructure C2 innovante :** Utilisation du réseau décentralisé IPFS et de la plateforme Pinata pour orchestrer le contrôle et la commande (C2) via le backdoor **KuboShell**.
*   **Framework d'attaque :** Déploiement de **Homa**, une réimplémentation en JavaScript du framework *MuddyC2Go*, complété par des outils RMM légitimes (MeshCentral, NetLock RMM).
*   **Persistance :** Le groupe adapte ses méthodes, passant d'un héritage technique MuddyWater à des outils propriétaires, tout en maintenant des campagnes de vol d'identifiants.

#### Vulnérabilités exploitées
*   **Ingénierie sociale :** Utilisation de documents Word piégés (macros VBA) et d'archives ZIP malveillantes.
*   **Escalade de privilèges :** KuboShell tente de se relancer avec des privilèges administrateur, déclenchant des invites UAC (User Account Control).
*   **Note :** Aucune CVE spécifique n'est mentionnée ; les attaques reposent sur l'exécution de scripts PowerShell et de macros malveillantes sur des systèmes Windows.

#### Recommandations
*   **Renforcement du filtrage email :** Bloquer les pièces jointes suspectes (fichiers .doc avec macros, archives .zip non sollicitées).
*   **Contrôle des privilèges :** Restreindre les droits d'administration locale pour empêcher les processus malveillants de s'élever.
*   **Surveillance réseau :** Surveiller les communications vers des passerelles IPFS publiques (ex: Pinata) et les connexions sortantes vers des adresses IP non identifiées associées aux frameworks de C2.
*   **Sensibilisation :** Former le personnel à la détection de CV frauduleux générés par IA et aux messages provenant de sources compromises (même au sein de partenaires de confiance).
*   **Détection RMM :** Auditer et restreindre l'utilisation des outils de gestion à distance (RMM) non autorisés au sein du parc informatique.

---
[Source](https://thehackernews.com/2026/11/iran-aligned-volant-manticore-uses-ipfs.html){:target="_blank"}
