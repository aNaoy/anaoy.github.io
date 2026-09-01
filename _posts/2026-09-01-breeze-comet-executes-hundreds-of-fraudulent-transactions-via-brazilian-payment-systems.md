---
title: 'Breeze Comet Executes Hundreds of Fraudulent Transactions via Brazilian Payment Systems'
date: 2026-09-01
permalink: /posts/2026/09/01/breeze-comet-executes-hundreds-of-fraudulent-transactions-via-brazilian-payment-systems/
tags:
- veille-cyber
- hackernews
---
### Menace financière : Le groupe Breeze Comet cible les infrastructures de paiement au Brésil

Le groupe cybercriminel **Breeze Comet** (anciennement UNC5669, également suivi sous les noms Plump Spider ou SHADOW-AETHER-064) mène depuis 2024 des intrusions sophistiquées contre les institutions financières, commerces et fintechs au Brésil. Ce groupe se distingue par sa capacité à manipuler directement les systèmes de paiement (Pix, STR, Boleto) pour détourner des fonds massifs.

#### Points clés
*   **Mode opératoire :** Utilisation d'ingénierie sociale (usurpation d'identité du support IT) et de tactiques de *password spraying*.
*   **Infrastructure :** Utilisation de sites gouvernementaux locaux compromis pour héberger des outils malveillants, facilitant le contournement des filtres de réputation.
*   **Automatisation :** Le groupe utilise des modèles de langage (LLM) pour accélérer le développement de malwares et optimiser ses scripts d'intrusion.
*   **Mouvement latéral :** Déploiement de **COBALTSPIN**, un outil en langage Rust créant un tunnel SOCKS5 via WebSocket pour traverser les pare-feu sans être détecté.
*   **Cibles :** Institutions ayant accès au réseau RSFN (National Financial System Network) et détenant des identifiants mTLS pour valider des transactions.

#### Vulnérabilités exploitées
*   **JBoss AS :** Exploitation de serveurs JBoss obsolètes pour déployer des *web shells*.
*   **Configuration AD/Cloud :** Exploitation des mauvaises configurations et vol de secrets via des sites de stockage de notes (ex: *dontpad[.]com*).
*   **Désactivation de la sécurité :** Utilisation de PowerShell pour neutraliser Windows Defender lors de la persistance.

#### Outils et Malwares identifiés
*   **Backdoors :** LIGHTPAINT (Java), MILDFROST (Java/DNS tunneling), KICKPLATE (Nim), BOATBEAM (Golang).
*   **Reconnaissance :** Impacket, ADRecon, ADVipscan, et l'outil propriétaire REALBREEZE.
*   **RMM :** Usage détourné d'AnyDesk et de scripts de télésurveillance.

#### Recommandations de sécurité
1.  **Renforcement des accès :** Appliquer une authentification multifacteur (MFA) stricte sur tous les comptes à privilèges, en particulier ceux ayant accès aux API de paiement.
2.  **Surveillance réseau :** Détecter les connexions inhabituelles de type *WebSocket* ou *SOCKS5* sortantes vers des infrastructures inconnues.
3.  **Gestion des correctifs :** Mettre à jour immédiatement les serveurs d'applications (type JBoss) et sécuriser les configurations Active Directory.
4.  **Politiques IT :** Sensibiliser le personnel à ne jamais installer d'outils de prise de contrôle à distance (RMM) suite à un appel téléphonique non vérifié.
5.  **Audit des terminaux :** Surveiller toute tentative de désactivation des services de sécurité (Windows Defender) via des scripts PowerShell automatisés.

---
[Source](https://thehackernews.com/2026/09/breeze-comet-executes-hundreds-of.html){:target="_blank"}
