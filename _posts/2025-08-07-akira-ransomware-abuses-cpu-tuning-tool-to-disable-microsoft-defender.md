---
title: 'Akira ransomware abuses CPU tuning tool to disable Microsoft Defender'
date: 2025-08-07
permalink: /posts/2025/08/07/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/
tags:
- veille-cyber
- bleepingcomp
---
## Akira : Sabotage des défenses via un pilote système détourné

Le groupe de rançongiciels Akira utilise une technique d'attaque dite "Bring Your Own Vulnerable Driver" (BYOVD) pour neutraliser Microsoft Defender sur les systèmes ciblés.

### Points Clés :

*   **Détournement de pilote Intel :** Akira exploite le pilote 'rwdrv.sys', légitime mais vulnérable (associé à ThrottleStop), pour obtenir un accès au niveau du noyau.
*   **Désactivation de Defender :** Ce pilote est utilisé pour charger un composant malveillant ('hlpdrv.sys') qui modifie les paramètres de Windows Defender pour désactiver ses protections, notamment la fonctionnalité anti-spyware.
*   **Méthode d'exécution :** L'altération des paramètres se fait par l'exécution de `regedit.exe`.
*   **Observed Attacks :** Cette tactique est observée dans les attaques d'Akira depuis juillet 2023.
*   **Attaques sur SonicWall :** Akira a également été associé à des attaques visant les VPN SSLVPN de SonicWall, potentiellement via une faille inconnue.
*   **Chaîne d'attaque :** D'autres vecteurs d'infection incluent l'utilisation du chargeur de malware Bumblebee, distribué via des installateurs MSI compromis de logiciels IT (par exemple, via le SEO poisoning), suivi par AdaptixC2 pour la persistance, l'exfiltration de données via FileZilla, et enfin le déploiement du rançongiciel Akira.

### Vulnérabilités :

Bien qu'aucun CVE spécifique ne soit mentionné pour le pilote 'rwdrv.sys' dans cet article, la méthode d'attaque est classée comme BYOVD, indiquant l'exploitation de faiblesses connues ou de vulnérabilités dans des pilotes légitimes et signés.

### Recommandations :

*   **Surveillance accrue :** Les administrateurs système doivent surveiller toute activité liée à Akira.
*   **Chasse aux menaces :** Utiliser des règles YARA (fournies par des chercheurs comme Guidepoint Security) pour détecter le pilote malveillant `hlpdrv.sys` et d'autres indicateurs de compromission (IoCs) associés aux pilotes utilisés par Akira.
*   **Sécurisation des VPN :** Pour les VPN SonicWall, envisager de désactiver ou restreindre l'accès SSLVPN, d'imposer l'authentification multifacteur (MFA) et d'activer la protection Botnet/Geo-IP.
*   **Sources logicielles sûres :** Télécharger les logiciels exclusivement à partir de sites officiels et de miroirs de confiance pour éviter les faux sites qui distribuent des malwares.
*   **Filtrage et blocage :** Appliquer des filtres et des blocages basés sur les indicateurs de compromission dès qu'ils sont disponibles grâce à la recherche en cybersécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/){:target="_blank"}
