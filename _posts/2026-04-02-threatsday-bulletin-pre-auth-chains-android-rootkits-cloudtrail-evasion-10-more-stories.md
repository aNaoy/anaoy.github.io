---
title: 'ThreatsDay Bulletin: Pre-Auth Chains, Android Rootkits, CloudTrail Evasion & 10 More Stories'
date: 2026-04-02
permalink: /posts/2026/04/02/threatsday-bulletin-pre-auth-chains-android-rootkits-cloudtrail-evasion-10-more-stories/
tags:
- veille-cyber
- hackernews
---
### Actualités de la menace : Chaînes RCE, Rootkits Android et évasion Cloud

Le paysage cyber actuel est marqué par une recrudescence d'attaques furtives, de chaînes de vulnérabilités et de compromissions de la chaîne d'approvisionnement logicielle.

#### Points clés
*   **Complexité accrue :** Les attaquants privilégient désormais l'enchaînement de failles mineures pour contourner l'authentification et l'exécution de code à distance (RCE).
*   **Chaîne d'approvisionnement :** Explosion des malwares dans les dépôts open-source (npm), ciblant des paquets largement utilisés pour maximiser l'impact.
*   **Furtivité Cloud :** Les attaquants neutralisent la surveillance AWS (CloudTrail) en utilisant des API détournées qui simulent des tâches de maintenance légitimes.
*   **Malwares Android :** Le rootkit "NoVoice" exploite d'anciennes vulnérabilités pour prendre le contrôle total des appareils et injecter du code malveillant dans d'autres applications.

#### Vulnérabilités critiques
*   **Progress ShareFile :** 
    *   **CVE-2026-2699 :** Contournement d'authentification.
    *   **CVE-2026-2701 :** RCE post-authentification.
    *   *Risque :* L'enchaînement permet une RCE pré-authentification complète.
*   **ImageMagick (Zero-days) :** Multiples failles permettant la RCE via le traitement d'images ou de PDF, non corrigées à ce jour.
*   **Android (Rootkit NoVoice) :** Utilise 22 vulnérabilités (2016-2021) pour escalader les privilèges et désactiver SELinux.

#### Recommandations
1.  **Correctifs immédiats :** Mettre à jour Progress ShareFile vers la version Storage Zone Controller 5.12.4.
2.  **Sécurisation ImageMagick :** Isoler le traitement des PDF dans des environnements sandbox sans accès réseau, désactiver XML-RPC sur WordPress et bloquer GhostScript.
3.  **Surveillance Cloud :** Auditer les configurations AWS pour détecter l'usage abusif d'API sensibles (`PutEventSelectors`, `StopEventDataStoreIngestion`, etc.), au-delà des simples alertes `StopLogging`.
4.  **Chaîne d'approvisionnement :** Renforcer les contrôles sur les dépendances open-source et monitorer les comportements suspects dans les pipelines CI/CD.
5.  **Hygiène mobile :** Se méfier des applications tierces, même proposées via des services légitimes (Firebase App Distribution), et limiter les accès accordés aux outils téléchargés hors des stores officiels.

---
[Source](https://thehackernews.com/2026/04/threatsday-bulletin-pre-auth-chains.html){:target="_blank"}
