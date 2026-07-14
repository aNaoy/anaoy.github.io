---
title: 'Microsoft July 2026 Patch Tuesday fixes massive 570 flaws, 3 zero-days'
date: 2026-07-14
permalink: /posts/2026/07/14/microsoft-july-2026-patch-tuesday-fixes-massive-570-flaws-3-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
### Record de vulnérabilités corrigées par Microsoft (Juillet 2026)

Le Patch Tuesday de juillet 2026 marque un record avec la correction de **570 vulnérabilités**, dont 59 sont classées comme « critiques ». Ce déploiement massif fait suite à la mise en œuvre d'un système de découverte de failles assisté par l'IA au sein de la base de code Windows.

#### Points clés
*   **Volume :** 570 vulnérabilités corrigées (excluant les correctifs Azure, Edge et les services cloud traités plus tôt dans le mois).
*   **Répartition des failles critiques :**
    *   48 vulnérabilités d'exécution de code à distance (RCE).
    *   9 vulnérabilités d'élévation de privilèges.
    *   1 vulnérabilité de contournement de sécurité.
    *   1 vulnérabilité de usurpation d'identité (spoofing).

#### Vulnérabilités Zero-Day actives
Trois vulnérabilités Zero-Day ont été identifiées, dont deux sont activement exploitées :

1.  **Active Directory Federation Services (AD FS) :**
    *   **Problème :** Élévation de privilèges locale due à une granularité insuffisante du contrôle d'accès.
    *   **Statut :** Activement exploitée.
2.  **Microsoft SharePoint Server :**
    *   **Problème :** Élévation de privilèges réseau due à une absence d'authentification pour une fonction critique.
    *   **Statut :** Activement exploitée.
3.  **Windows BitLocker :**
    *   **Problème :** Contournement de la sécurité permettant l'accès aux données chiffrées en cas d'accès physique.
    *   **Statut :** Divulguée publiquement.

#### Recommandations
*   **Application immédiate :** Déployer les correctifs de sécurité fournis par Microsoft pour l'ensemble du parc informatique afin de neutraliser les failles RCE et les élévations de privilèges.
*   **Atténuation SharePoint :** Pour la faille SharePoint, Microsoft préconise d'activer l'interface **Antimalware Scan Interface (AMSI)** sur le serveur et de configurer le mode *Request Body Scan* sur **Full**.
*   **Sécurisation physique :** En raison de la faille BitLocker, renforcer les protocoles de sécurité physique pour les appareils portables afin de prévenir l'accès non autorisé aux disques chiffrés.
*   **Surveillance :** Maintenir une veille active sur les rapports complets publiés par Microsoft, car le volume élevé de correctifs (notamment pour .NET, SharePoint et divers services Windows) nécessite une planification rigoureuse des redémarrages et tests de compatibilité.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-july-2026-patch-tuesday-fixes-massive-570-flaws-3-zero-days/){:target="_blank"}
