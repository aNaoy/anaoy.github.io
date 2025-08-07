---
title: 'Akira ransomware abuses CPU tuning tool to disable Microsoft Defender'
date: 2025-08-07
permalink: /posts/2025/08/07/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/
tags:
- veille-cyber
- bleepingcomp
---
### Akira : Désactivation de la protection Microsoft Defender via un pilote légitime

Le groupe de ransomware Akira utilise une technique d'attaque BYOVD (Bring Your Own Vulnerable Driver) pour désactiver Microsoft Defender sur les systèmes compromis.

**Points Clés :**

*   Akira exploite un pilote légitime d'Intel, `rwdrv.sys` (associé à ThrottleStop), en l'enregistrant comme service pour obtenir un accès au niveau du noyau.
*   Ce pilote est ensuite utilisé pour charger un second pilote, `hlpdrv.sys`, dont le but est de modifier les paramètres de Windows Defender afin de désactiver ses protections.
*   La modification se fait en exécutant `regedit.exe` pour changer la valeur de `DisableAntiSpyware` dans le registre Windows.
*   Cette tactique a été observée dans des attaques d'Akira depuis juillet 2025.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée pour le pilote `rwdrv.sys` dans cet article, mais son abus est lié à des faiblesses exploitables.

**Recommandations :**

*   Surveiller l'activité liée à Akira et appliquer des filtres et blocages basés sur les indicateurs de compromission (IoCs) émergeant de la recherche en sécurité.
*   Désactiver ou restreindre l'accès à SonicWall SSLVPN.
*   Mettre en œuvre l'authentification multifacteur (MFA).
*   Activer la protection contre les botnets et le filtrage par adresse IP géographique (Geo-IP).
*   Supprimer les comptes utilisateurs inutilisés.
*   Télécharger les logiciels exclusivement à partir de sites officiels et de miroirs pour éviter les sites d'impersonation qui distribuent des malwares.
*   Utiliser des règles YARA pour la détection du pilote `hlpdrv.sys` et des IoCs fournis par les chercheurs en sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/){:target="_blank"}
