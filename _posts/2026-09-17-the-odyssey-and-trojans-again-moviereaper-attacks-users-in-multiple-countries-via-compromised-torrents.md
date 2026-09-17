---
title: 'The Odyssey and trojans again: MovieReaper attacks users in multiple countries via compromised torrents'
date: 2026-09-17
permalink: /posts/2026/09/17/the-odyssey-and-trojans-again-moviereaper-attacks-users-in-multiple-countries-via-compromised-torrents/
tags:
- veille-cyber
- securelist
---
### Campagne MovieReaper : Une menace modulaire via les réseaux Torrent

La campagne **MovieReaper** cible des particuliers et des organisations à travers le monde en détournant le dépôt public *itorrents[.]org*. Les attaquants injectent des torrents malveillants, déguisés en contenus multimédias populaires, pour déployer un malware modulaire et multi-étapes capable d'exécuter des commandes à distance.

**Points clés :**
*   **Vecteur d'infection :** Téléchargement de fichiers corrompus via des sites de torrents utilisant le dépôt compromis *itorrents[.]org*.
*   **Architecture modulaire :** Le malware utilise une chaîne d'infection en plusieurs étapes, incluant un chargeur, un shellcode et un module final de gestion de fichiers.
*   **Résilience C2 :** Pour éviter les blocages classiques, les attaquants utilisent la blockchain Solana pour récupérer dynamiquement l'adresse de leur serveur de commande et de contrôle (C2).
*   **Evasion :** Le logiciel malveillant intègre des techniques anti-sandbox (parsing manuel de DLL, exécution en mémoire, syscalls directs) et des mécanismes de contournement de l'UAC pour assurer sa persistance.

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; le malware s'appuie sur le comportement humain (incitation à désactiver l'antivirus lors de l'installation de logiciels piratés) et sur des techniques standards de persistance Windows.

**Recommandations :**
*   **Vigilance sur les contenus piratés :** Éviter de télécharger des exécutables à partir de sites torrent non sécurisés ou de sources non vérifiées.
*   **Protection des endpoints :** Maintenir les solutions de sécurité à jour. La détection Kaspersky identifie cette menace sous le nom `HEUR:Trojan.Win64.Agent.gen`.
*   **Sensibilisation :** Ne jamais désactiver les logiciels de sécurité pour installer un logiciel tiers, une pratique couramment exploitée par les attaquants pour garantir le succès de l'infection.
*   **Surveillance réseau :** Surveiller les connexions sortantes vers les domaines et IP suspects cités (ex: `deadhub[.]org`, `193.23.118[.]155`) et filtrer les accès aux services RPC de la blockchain Solana si nécessaire dans un environnement d'entreprise.

---
[Source](https://securelist.com/moviereaper-malware-torrent-odyssey-solana/121344/){:target="_blank"}
