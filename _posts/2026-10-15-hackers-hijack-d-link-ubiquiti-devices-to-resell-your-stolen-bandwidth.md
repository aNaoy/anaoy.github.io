---
title: 'Hackers hijack D-Link, Ubiquiti devices to resell your stolen bandwidth'
date: 2026-10-15
permalink: /posts/2026/10/15/hackers-hijack-d-link-ubiquiti-devices-to-resell-your-stolen-bandwidth/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement de bande passante : la menace du "Proxyjacking"

Une campagne de cyberattaques cible des appareils en périphérie de réseau (NAS, NVR, DVR) dans 34 pays pour transformer ces équipements en nœuds de sortie de réseaux proxy résidentiels. Les attaquants installent à l'insu des propriétaires l'application légitime *Pawns.app* afin de monétiser la bande passante volée, exposant ainsi les victimes à des risques juridiques et à des blocages d'adresses IP.

**Points clés :**
* **Méthode :** Exploitation de vulnérabilités sur des appareils exposés sur Internet pour y installer des logiciels de partage de connexion.
* **Persistance :** Les attaquants ajoutent fréquemment des clés SSH pour garantir un accès permanent aux appareils compromis.
* **Impact :** Utilisation des connexions des victimes pour des activités malveillantes, comme des attaques par bourrage d'identifiants (*credential stuffing*).

**Vulnérabilités exploitées :**
* **D-Link ShareCenter NAS :** CVE-2024-3272 et CVE-2024-3273.
* **Ubiquiti UniFi Video NVR :** CVE-2021-44228.
* **SAP NetWeaver Visual Composer :** CVE-2025-31324.
* *Note : Des équipements Hikvision et Dahua sont également ciblés via des failles non spécifiées.*

**Recommandations :**
* **Mises à jour :** Appliquer immédiatement les correctifs de sécurité sur tous les appareils connectés (NAS, enregistreurs vidéo, routeurs).
* **Durcissement :** Utiliser des mots de passe robustes et restreindre l'accès réseau à distance.
* **Audit :** Vérifier les configurations SSH pour détecter toute clé d'accès non autorisée.
* **Surveillance :** Utiliser des outils de renseignement sur les menaces (comme ceux proposés par GreyNoise) pour vérifier si une adresse IP est utilisée comme nœud de proxy.
* **Hygiène logicielle :** Éviter l'installation de logiciels provenant de sources non fiables.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hijack-d-link-ubiquiti-devices-to-resell-your-stolen-bandwidth/){:target="_blank"}
