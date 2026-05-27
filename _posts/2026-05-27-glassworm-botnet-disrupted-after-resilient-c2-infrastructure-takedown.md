---
title: 'Glassworm botnet disrupted after resilient C2 infrastructure takedown'
date: 2026-05-27
permalink: /posts/2026/05/27/glassworm-botnet-disrupted-after-resilient-c2-infrastructure-takedown/
tags:
- veille-cyber
- bleepingcomp
---
### Neutralisation du botnet Glassworm : démantèlement d'une infrastructure résiliente

Le botnet Glassworm, actif depuis octobre 2025, a été mis hors d'état de nuire par une opération coordonnée entre CrowdStrike, Google et The Shadowserver Foundation. Ce malware ciblait spécifiquement les développeurs via des extensions malveillantes (OpenVSX, VS Code), des dépôts GitHub et des paquets npm afin de dérober des identifiants et des portefeuilles de cryptomonnaies.

**Points clés :**
* **Nature de la menace :** Attaques par empoisonnement de la chaîne d'approvisionnement logicielle (« supply-chain attacks »).
* **Innovation technique :** Le botnet utilisait une infrastructure de commande et contrôle (C2) hautement résiliente, conçue pour éviter tout point de défaillance unique.
* **Complexité du démantèlement :** La neutralisation a nécessité la coupure simultanée de quatre canaux de communication distincts.

**Architecture de l'infrastructure C2 :**
1. **Blockchain Solana :** Utilisation des champs « memo » des transactions pour stocker des adresses C2 immuables.
2. **Réseau BitTorrent DHT :** Requêtes sur des clés publiques pour récupérer des données de configuration.
3. **Services de calendrier public :** Utilisation de Google Calendar pour dissimuler des chemins C2 encodés en Base64.
4. **Serveurs VPS traditionnels :** Livraison finale des charges utiles malveillantes.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car la menace repose sur des vecteurs de distribution légitimes (extensions IDE, dépôts de code) et non sur l'exploitation de failles logicielles classiques. Le risque réside dans l'exécution de code arbitraire lors de l'installation ou de la mise à jour d'extensions compromises.

**Recommandations :**
* **Détection :** Rechercher les traces réseau pointant vers l'adresse IP `164.92.88.210` (contrôlée par CrowdStrike) pour identifier les machines infectées.
* **Audit :** Utiliser les règles YARA publiées par les chercheurs pour scanner les hôtes suspects et confirmer une compromission.
* **Remédiation :** Supprimer immédiatement toute extension ou paquet suspect identifié dans les environnements de développement et réinitialiser les identifiants compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/glassworm-botnet-disrupted-after-resilient-c2-infrastructure-takedown/){:target="_blank"}
