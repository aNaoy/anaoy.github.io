---
title: 'Rogue ScreenConnect Clients Spread Four-Stage VBScript Chain to Newly Connected Hosts'
date: 2026-09-07
permalink: /posts/2026/09/07/rogue-screenconnect-clients-spread-four-stage-vbscript-chain-to-newly-connected-hosts/
tags:
- veille-cyber
- hackernews
---
### Propagation de malwares via des clients ScreenConnect compromis

Des chercheurs ont identifié une campagne de cyberattaques utilisant des clients **ConnectWise ScreenConnect** détournés pour déployer une chaîne d'infection en quatre étapes par scripts VBScript. Cette méthode présente un comportement de type « ver », où la connexion à un client infecté provoque la contamination du système hôte distant.

**Points clés :**
*   **Vecteurs d'infection initiaux :** Escroqueries au support technique (Quick Assist), phishing (installateurs MSI malveillants) et faux formulaires de remboursement.
*   **Chaîne d'exécution :** Quatre scripts VBScript (`1.vbs` à `4.vbs`) profilent la machine, contournent l'UAC, assurent la persistance et téléchargent des charges utiles via Dropbox.
*   **Comportement adaptatif :** Le script `1.vbs` analyse l'environnement (RAM, antivirus installés comme CrowdStrike ou SentinelOne) et génère un état (variable sur 3 bits) pour déterminer la charge utile finale.
*   **Payloads observés :** Backdoors pour accès à distance, outils d'escalade de privilèges, logiciels de tunneling et mineurs de cryptomonnaie (XMRig).
*   **Persistance :** Utilisation de clés de registre « Run » et suppression des traces post-exécution.

**Vulnérabilités :**
*   Le problème réside dans une exploitation abusive des fonctionnalités de transfert de fichiers de ConnectWise ScreenConnect. Aucun identifiant CVE spécifique n'est mentionné, mais l'éditeur a confirmé une faille dans la gestion des transferts de fichiers (impactant le Cloud et le sur site).

**Recommandations :**
*   **Action immédiate :** Désactiver les permissions `TransferFiles` (ou `TransferFilesInSession`) pour les rôles d'utilisateurs dans l'interface d'administration de ScreenConnect afin d'empêcher l'exécution des scripts via le transfert de fichiers.
*   **Remédiation des systèmes infectés :** En cas de compromission, il est fortement conseillé de réinstaller entièrement le système d'exploitation à partir d'une source saine (« re-imaging »), plutôt que de tenter un nettoyage manuel.
*   **Surveillance :** Auditer les instances ScreenConnect pour détecter des connexions inattendues vers des adresses IP suspectes ou la présence de scripts VBScript dans les répertoires temporaires.

---
[Source](https://thehackernews.com/2026/09/rogue-screenconnect-clients-spread-four.html){:target="_blank"}
