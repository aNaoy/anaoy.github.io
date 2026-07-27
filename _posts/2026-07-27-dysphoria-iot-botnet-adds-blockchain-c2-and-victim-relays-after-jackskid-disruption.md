---
title: 'Dysphoria IoT Botnet Adds Blockchain C2 and Victim Relays After JackSkid Disruption'
date: 2026-07-27
permalink: /posts/2026/07/27/dysphoria-iot-botnet-adds-blockchain-c2-and-victim-relays-after-jackskid-disruption/
tags:
- veille-cyber
- hackernews
---
### Évolution du botnet IoT Dysphoria : résilience par la blockchain

Le botnet **Dysphoria** a émergé comme le successeur direct du botnet *JackSkid*, démantelé par une opération internationale en mars 2026. Cette nouvelle variante se distingue par une architecture hautement résiliente, conçue pour contrer les saisies d'infrastructures classiques.

**Points clés :**
*   **Infrastructure décentralisée :** Le botnet utilise désormais des services de noms basés sur la blockchain (ENS pour Ethereum et SNS pour Solana) pour résoudre ses serveurs de commande et contrôle (C2).
*   **Système de relais :** Dysphoria transforme ses propres machines infectées en nœuds de relais, masquant ainsi l'adresse IP réelle des serveurs de pilotage.
*   **Fonctionnalités avancées :** Le malware intègre le mappage de ports via UPnP pour traverser les passerelles NAT et utilise le chiffrement RC4 pour ses chaînes de caractères.
*   **Menace persistante :** Estimé à plus de 200 000 appareils, le botnet est principalement utilisé pour des attaques DDoS dont la puissance annoncée atteint 4 Tbps.

**Vulnérabilités exploitées :**
*   Utilisation massive d'identifiants par défaut ou faibles via Telnet et SSH.
*   **CVE-2025-9528 :** Vulnérabilité d'injection de commande dans les routeurs Linksys E1700.
*   Diverses failles d'exécution de code à distance (RCE) sur des routeurs, passerelles et caméras connectées.

**Recommandations :**
*   Appliquer systématiquement les correctifs de sécurité sur tous les équipements IoT.
*   Remplacer les matériels obsolètes ne recevant plus de mises à jour constructeur.
*   Désactiver les services inutilisés tels que l'UPnP et l'administration à distance (Remote Management).
*   Renforcer l'accès aux appareils en modifiant les identifiants par défaut par des mots de passe robustes et en désactivant Telnet au profit de protocoles sécurisés.

---
[Source](https://thehackernews.com/2026/07/dysphoria-iot-botnet-adds-blockchain-c2.html){:target="_blank"}
