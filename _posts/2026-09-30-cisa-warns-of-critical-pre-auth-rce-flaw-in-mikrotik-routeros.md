---
title: 'CISA warns of critical pre-auth RCE flaw in MikroTik RouterOS'
date: 2026-09-30
permalink: /posts/2026/09/30/cisa-warns-of-critical-pre-auth-rce-flaw-in-mikrotik-routeros/
tags:
- veille-cyber
- bleepingcomp
---
### Alerte de sécurité : Vulnérabilité critique dans MikroTik RouterOS

La CISA a émis une alerte concernant une faille critique affectant MikroTik RouterOS, permettant à un attaquant distant d'exécuter du code arbitraire avec des privilèges root ou de provoquer un déni de service sans nécessiter d'authentification.

**Points clés :**
*   La vulnérabilité réside dans le service de gestion web (HTTP) de RouterOS.
*   Une seule requête malveillante suffit pour exploiter la faille avant authentification.
*   Bien qu'aucune exploitation active ne soit rapportée, les équipements MikroTik sont régulièrement ciblés par des botnets.

**Vulnérabilité :**
*   **CVE-2026-84411** : Dépassement d'entier (integer underflow) dans la gestion des requêtes HTTP.
*   **Versions affectées** : Versions antérieures à 7.24.

**Recommandations :**
*   **Mise à jour immédiate** : Installer la version 7.24.4 (stable) ou 7.23.7 (long-term) ou toute version ultérieure.
*   **Isolation réseau** : Rendre les systèmes de contrôle inaccessibles directement depuis internet.
*   **Segmentation** : Placer les réseaux de contrôle et les périphériques distants derrière des pare-feu, isolés des réseaux d'entreprise.
*   **Accès distant sécurisé** : Utiliser exclusivement des VPN mis à jour pour accéder aux équipements et sécuriser l'ensemble des appareils connectés.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-warns-of-critical-pre-auth-rce-flaw-in-mikrotik-routeros/){:target="_blank"}
