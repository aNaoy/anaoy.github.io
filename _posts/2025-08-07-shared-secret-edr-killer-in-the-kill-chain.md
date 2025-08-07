---
title: 'Shared secret: EDR killer in the kill chain'
date: 2025-08-07
permalink: /posts/2025/08/07/shared-secret-edr-killer-in-the-kill-chain/
tags:
- veille-cyber
- sophos
---
## Le fléau des tueurs d'EDR : une menace coopérative

Les groupes de ransomware développent et partagent des outils sophistiqués pour désactiver les solutions de sécurité Endpoint Detection and Response (EDR). Ces malwares, souvent obscurcis par des packers comme HeartCrypt, sont devenus des éléments clés dans les chaînes d'attaque multi-étapes.

**Points clés :**

*   **Augmentation de la sophistication :** Depuis 2022, on observe une hausse des malwares conçus pour neutraliser les EDR.
*   **Partage d'outils :** Des preuves indiquent un partage d'outils et de connaissances techniques entre différents groupes de ransomware concurrents, notamment RansomHub, BlackBasta, Qilin, DragonForce et INC.
*   **HeartCrypt :** Ce packer "as-a-service" est largement utilisé pour masquer ces outils de désactivation d'EDR, suggérant une coordination potentielle dans l'écosystème du ransomware.
*   **Technique d'injection :** Des malwares injectent du code malveillant dans des utilitaires légitimes, comme Beyond Compare, pour contourner la détection.

**Vulnérabilités et Artefacts :**

Les malwares analysés présentent plusieurs caractéristiques notables :

*   **Code fortement protégé.**
*   **Recherche d'un pilote spécifique** (ex: `mraml.sys` avec le hash SHA-1 `21a9ca6028992828c9c360d752cb033603a2fd93`).
*   **Utilisation de certificats compromis ou expirés** pour signer les pilotes malveillants (ex: `Changsha Hengxiang Information Technology Co., Ltd.`, `Fuzhou Dingxin Trade Co., Ltd.`). Ces certificats sont souvent révoqués.
*   **Ciblage d'un large éventail de produits de sécurité :** Bitdefender, Cylance, F-Secure, Fortinet, Kaspersky, McAfee, Microsoft, SentinelOne, Sophos, Symantec, Trend Micro, Webroot, Eset, HitManPro.
*   **Terminaison de processus/services de sécurité :** `MsMpEng.exe`, `SophosHealth.exe`, `SAVService.exe`, `sophosui.exe`.
*   **Exemples de malwares :**
    *   `uA8s.exe` (SHA-1: `2bc75023f6a4c50b21eb54d1394a7b8417608728`)
    *   Variantes de `AVKiller`
*   **Utilisation dans des attaques de ransomware :** Les groupes observés incluent RansomHub, Blacksuit, Medusa, Qilin, DragonForce, Crytox, Lynx et INC.

**Recommandations :**

Bien que l'article ne fournisse pas de liste exhaustive de recommandations, la nature de la menace suggère :

*   **Surveillance accrue des processus et des pilotes suspects.**
*   **Mise à jour régulière des solutions de sécurité** et application des correctifs.
*   **Vigilance face aux utilitaires légitimes potentiellement détournés.**
*   **Analyse des certificats numériques** pour identifier les certificats révoqués ou suspects.
*   **Renforcement des mesures de détection et de prévention des menaces avancées.**

Les indicateurs de compromission (IOCs) sont disponibles dans le dépôt GitHub de Sophos Labs.

---
[Source](https://news.sophos.com/en-us/2025/08/06/shared-secret-edr-killer-in-the-kill-chain/){:target="_blank"}
