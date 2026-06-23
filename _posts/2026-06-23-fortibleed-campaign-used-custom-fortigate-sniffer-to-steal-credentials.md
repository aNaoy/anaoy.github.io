---
title: 'FortiBleed campaign used custom FortiGate sniffer to steal credentials'
date: 2026-06-23
permalink: /posts/2026/06/23/fortibleed-campaign-used-custom-fortigate-sniffer-to-steal-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### La campagne « FortiBleed » : Espionnage et vol d'identifiants via FortiGate

La campagne « FortiBleed », active depuis février 2026, cible massivement les pare-feux Fortinet FortiGate (plus de 430 000 appareils visés). Les attaquants agissent comme des courtiers en accès initial en exploitant des fonctionnalités légitimes pour intercepter des données sensibles au sein des réseaux d'entreprise.

**Points clés :**
*   **Mode opératoire :** Après avoir obtenu un accès administratif via des attaques par force brute ou « credential stuffing », les attaquants déploient un outil personnalisé nommé « FortigateSniffer ».
*   **Détournement fonctionnel :** L'outil abuse de la commande native `diagnose sniffer packet` de FortiOS pour capturer en temps réel le trafic réseau passant par le pare-feu.
*   **Extraction de données :** Le trafic capturé (24 protocoles dont RADIUS, NTLM, Kerberos, LDAP, SMB, etc.) est traité par le composant « SNIFTRAN » pour générer des fichiers PCAP, ensuite analysés par un toolkit Python pour extraire identifiants en clair et hashs.
*   **Puissance de calcul :** Les hashs extraits sont craqués massivement à l'aide de clusters de GPU professionnels (jusqu'à 36 unités louées auprès de fournisseurs cloud).

**Vulnérabilités :**
*   Aucune vulnérabilité logicielle (CVE) spécifique n'est exploitée ; les attaquants utilisent des fonctionnalités légitimes d'administration et des méthodes d'authentification faibles.

**Recommandations :**
*   **Audit d'accès :** Renforcer les mécanismes d'authentification (MFA obligatoire) pour prévenir l'accès administratif initial.
*   **Surveillance :** Inspecter les logs pour détecter l'usage inhabituel ou non autorisé de la commande `diagnose sniffer packet`.
*   **Analyse d'exposition :** Consulter les listes d'adresses IP connues liées à la campagne (publiées par des chercheurs comme Kevin Beaumont) pour vérifier si des équipements ont été ciblés.
*   **Gestion des identifiants :** Procéder à une réinitialisation des mots de passe et des secrets Kerberos/NTLM pour les comptes ayant transité par les équipements FortiGate potentiellement compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/fortibleed-campaign-used-custom-fortigate-sniffer-to-steal-credentials/){:target="_blank"}
