---
title: 'New Windows RasMan zero-day flaw gets free, unofficial patches'
date: 2025-12-12
permalink: /posts/2025/12/12/new-windows-rasman-zero-day-flaw-gets-free-unofficial-patches/
tags:
- veille-cyber
- bleepingcomp
---
### Une faille critique dans le service RasMan de Windows découverte, des correctifs non officiels disponibles

Une nouvelle vulnérabilité **zero-day** a été identifiée dans le service **Remote Access Connection Manager (RasMan)** de Windows. Ce service, essentiel à la gestion des connexions réseau à distance comme les VPN, fonctionnant avec des privilèges système, peut être exploité pour provoquer un déni de service (DoS).

La faille, découverte par ACROS Security, est due à une mauvaise gestion des listes chaînées circulaires par le service. Lorsqu'il rencontre un pointeur nul lors de la traversée d'une liste, il tente de lire une mémoire invalide au lieu de s'arrêter, entraînant un plantage.

Bien qu'un correctif officiel n'ait pas encore été publié par Microsoft, ACROS Security propose des **micropatches gratuits et non officiels** via sa plateforme 0patch. Ces correctifs sont disponibles pour toutes les versions affectées de Windows, de Windows 7 à Windows 11 et les serveurs associés, jusqu'à ce qu'une mise à jour officielle soit distribuée.

**Points clés :**

*   **Service affecté :** Remote Access Connection Manager (RasMan) de Windows.
*   **Type de vulnérabilité :** Déni de service (DoS) par plantage du service.
*   **Cause :** Erreur de traitement des pointeurs nuls dans les listes chaînées circulaires.
*   **Impact potentiel :** Permet aux attaquants de planter le service, ce qui peut potentiellement faciliter des attaques d'escalade de privilèges, notamment en combinaison avec d'autres vulnérabilités (comme CVE-2025-59230).
*   **Version actuelle :** La faille n'a pas encore reçu de numéro CVE.
*   **Correctifs :** Des micropatches non officiels gratuits sont disponibles chez ACROS Security (0patch).

**Vulnérabilités :**

*   **Zero-day non identifiée par CVE :** Permet un déni de service sur le service RasMan.
*   **CVE-2025-59230 :** Vulnérabilité d'escalade de privilèges dans RasMan, corrigée en octobre, qui peut être combinée avec la zero-day pour des attaques plus avancées.

**Recommandations :**

*   Installer les **micropatches non officiels** fournis par ACROS Security pour une protection immédiate.
*   Créer un compte sur la plateforme 0patch et installer l'agent 0Patch pour déployer automatiquement le micropatch.
*   Rester vigilant et attendre la publication d'un **correctif officiel** de la part de Microsoft pour les versions de Windows encore supportées.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/new-windows-rasman-zero-day-flaw-gets-free-unofficial-patches/){:target="_blank"}
