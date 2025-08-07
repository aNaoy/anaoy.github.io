---
title: 'Akira ransomware abuses CPU tuning tool to disable Microsoft Defender'
date: 2025-08-07
permalink: /posts/2025/08/07/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation d'un Pilote Intel par Akira pour Désactiver Microsoft Defender

Le groupe Akira utilise un pilote légitime d'Intel, `rwdrv.sys` (associé à ThrottleStop), pour obtenir un accès au niveau du noyau sur les systèmes ciblés. Ce pilote est enregistré comme service et utilisé pour charger un deuxième pilote malveillant, `hlpdrv.sys`. Ce dernier a pour fonction de désactiver les protections de Microsoft Defender en modifiant les paramètres de registre spécifiques (comme `DisableAntiSpyware`). Cette technique, connue sous le nom de "Bring Your Own Vulnerable Driver" (BYOVD), tire parti de failles ou de faiblesses dans des pilotes légitimes et signés pour obtenir une escalade de privilèges.

**Points Clés :**

*   **Méthode :** Le groupe Akira exploite le pilote `rwdrv.sys` (Intel CPU tuning driver) pour masquer ses activités et désactiver la protection antivirus.
*   **Technique :** Utilisation d'une attaque BYOVD (Bring Your Own Vulnerable Driver).
*   **Pilotes impliqués :** `rwdrv.sys` (légitime, utilisé pour escalader les privilèges) et `hlpdrv.sys` (malveillant, désactive Microsoft Defender).
*   **Objectif :** Désactivation de Microsoft Defender pour faciliter le déploiement du ransomware.
*   **Observation :** Cette tactique est observée de manière récurrente dans les attaques Akira depuis mi-juillet 2025.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée dans l'article pour la vulnérabilité directe de `rwdrv.sys` elle-même. L'exploitation repose sur l'abus de ses fonctionnalités dans un contexte non prévu par l'éditeur pour l'escalade de privilèges.

**Recommandations :**

*   **Détection :** Utiliser des règles YARA pour détecter `hlpdrv.sys` et surveiller les indicateurs de compromission (IoCs) liés à `rwdrv.sys` et `hlpdrv.sys`, y compris leurs noms de service et chemins de fichiers.
*   **Sécurité VPN :** Dans le cas d'attaques récentes sur SonicWall SSLVPN, il est conseillé de désactiver ou restreindre l'accès SSLVPN, de renforcer l'authentification multifacteur (MFA), et d'activer la protection contre les botnets/Geo-IP.
*   **Sources logicielles :** Télécharger les logiciels exclusivement depuis les sites officiels et les miroirs autorisés pour éviter les sites d'usurpation servant de vecteurs d'infection.
*   **Surveillance :** Maintenir une vigilance accrue pour les activités liées à Akira et appliquer les blocages et filtres basés sur les informations de sécurité émergentes.

---
[Source](https://www.bleepingcomputer.com/news/security/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/){:target="_blank"}
