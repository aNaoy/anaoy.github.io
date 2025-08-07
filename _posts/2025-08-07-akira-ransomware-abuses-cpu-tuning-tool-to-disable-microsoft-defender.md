---
title: 'Akira ransomware abuses CPU tuning tool to disable Microsoft Defender'
date: 2025-08-07
permalink: /posts/2025/08/07/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/
tags:
- veille-cyber
- bleepingcomp
---
### Akira : Le Ransomware qui Désactive Microsoft Defender

Le groupe Akira utilise un pilote de réglage CPU légitime d'Intel, 'rwdrv.sys' (associé à ThrottleStop), pour obtenir un accès au niveau du noyau sur les systèmes cibles. Ce pilote sert ensuite à charger un second pilote malveillant, 'hlpdrv.sys', conçu pour désactiver les protections de Microsoft Defender. Cette technique, connue sous le nom de "Bring Your Own Vulnerable Driver" (BYOVD), exploite les vulnérabilités de pilotes signés légitimement pour obtenir des privilèges élevés. Le pilote malveillant modifie les paramètres de Windows Defender via l'exécution de `regedit.exe`.

**Points Clés :**

*   Le ransomware Akira utilise un pilote Intel légitime ('rwdrv.sys') pour désactiver Microsoft Defender.
*   Une attaque BYOVD est employée, consistant à utiliser un pilote signé mais vulnérable pour charger un outil malveillant.
*   Le pilote malveillant ('hlpdrv.sys') modifie les clés de registre de Windows Defender pour désactiver ses protections.
*   Cette tactique est observée dans les attaques Akira depuis juillet 2023.
*   Les attaques Akira ont également été associées à des exploitations potentielles de vulnérabilités sur les VPN SonicWall SSLVPN.
*   Une autre chaîne d'attaque implique le chargeur de malware Bumblebee, livré via des installateurs MSI compromis d'outils IT, menant à l'évasion, à l'exfiltration de données et au déploiement du ransomware.

**Vulnérabilités :**

*   Le pilote 'rwdrv.sys' (associé à ThrottleStop) est le composant principal exploité. Aucune CVE spécifique n'est mentionnée pour ce pilote dans l'article, mais il est décrit comme ayant des "vulnérabilités ou faiblesses connues" exploitables.
*   Une possible vulnérabilité zero-day dans les VPN SonicWall SSLVPN est suggérée dans le contexte d'attaques Akira, mais non confirmée par les chercheurs.

**Recommandations :**

*   **Pour la détection :** Utiliser une règle YARA fournie par Guidepoint Security pour détecter 'hlpdrv.sys'. Surveiller l'apparition de pilotes 'rwdrv.sys' et 'hlpdrv.sys', leurs noms de services et les chemins de fichiers où ils sont déposés.
*   **Sécurisation VPN SonicWall :** Suivre les conseils de SonicWall : désactiver ou restreindre SSLVPN, renforcer l'authentification multifacteur (MFA), activer la protection Botnet/Geo-IP et supprimer les comptes inutilisés.
*   **Pratiques Générales :** Télécharger les logiciels uniquement depuis des sites officiels et leurs miroirs pour éviter les sites d'usurpation qui distribuent des malwares. Surveiller l'activité liée à Akira et appliquer des filtres et des blocages basés sur les indicateurs de compromission émergents.

---
[Source](https://www.bleepingcomputer.com/news/security/akira-ransomware-abuses-cpu-tuning-tool-to-disable-microsoft-defender/){:target="_blank"}
