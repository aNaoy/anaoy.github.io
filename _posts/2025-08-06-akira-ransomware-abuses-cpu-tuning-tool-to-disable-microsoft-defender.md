---
title: 'Akira ransomware abuses CPU tuning tool to disable Microsoft Defender'
date: 2025-08-06
permalink: /posts/2025/08/06/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/
tags:
- veille-cyber
- bleepingcomp
---
### Akira Ransomware Utilise des Outils Légitimes pour Désactiver Microsoft Defender

Le groupe Akira exploite un pilote de réglage du processeur Intel, `rwdrv.sys` (associé à ThrottleStop), pour obtenir un accès au niveau du noyau et désactiver Microsoft Defender sur les systèmes ciblés. Cette technique, qualifiée d'attaque "Bring Your Own Vulnerable Driver" (BYOVD), permet aux acteurs malveillants de charger un second pilote, `hlpdrv.sys`, qui modifie les paramètres de Windows Defender via le registre (`DisableAntiSpyware`) pour désactiver ses protections. Cette méthode a été observée dans plusieurs attaques récentes d'Akira, notamment contre des environnements SonicWall SSLVPN.

**Points Clés :**

*   **Exploitation d'un pilote légitime :** Le pilote `rwdrv.sys` d'Intel est enregistré comme service pour obtenir des privilèges élevés.
*   **Désactivation de Defender :** Un pilote malveillant (`hlpdrv.sys`) est utilisé pour modifier des clés de registre afin de désactiver les fonctionnalités de sécurité de Microsoft Defender.
*   **Type d'attaque :** Il s'agit d'une attaque BYOVD (Bring Your Own Vulnerable Driver).
*   **Liens avec SonicWall :** Cette tactique a été constatée dans des attaques visant les VPN SonicWall.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques pour le pilote `rwdrv.sys`. Il s'agit plutôt d'une faiblesse ou d'une méthode d'abus connue de ce pilote légitime.

**Recommandations :**

*   **Surveillance des pilotes :** Surveiller l'enregistrement et l'exécution de pilotes non reconnus ou suspects, en particulier `rwdrv.sys` et `hlpdrv.sys`.
*   **Protection SonicWall :** Désactiver ou restreindre l'utilisation de SSLVPN, renforcer l'authentification multifacteur (MFA) et activer la protection Botnet/Geo-IP sur les systèmes SonicWall.
*   **Téléchargement de logiciels :** Ne télécharger des logiciels que depuis des sites officiels et des miroirs pour éviter les sites d'usurpation qui distribuent des malwares.
*   **Chasse aux menaces :** Utiliser des règles YARA et des indicateurs de compromission (IoCs) pour détecter les activités liées à Akira et aux pilotes associés.

---
[Source](https://www.bleepingcomputer.com/news/security/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/){:target="_blank"}
