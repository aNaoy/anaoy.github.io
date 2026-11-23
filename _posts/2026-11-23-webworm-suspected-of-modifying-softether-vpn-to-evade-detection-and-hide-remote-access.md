---
title: 'Webworm Suspected of Modifying SoftEther VPN to Evade Detection and Hide Remote Access'
date: 2026-11-23
permalink: /posts/2026/11/23/webworm-suspected-of-modifying-softether-vpn-to-evade-detection-and-hide-remote-access/
tags:
- veille-cyber
- hackernews
---
### Webworm : Utilisation détournée de SoftEther VPN pour une exfiltration furtive

Le groupe de menace persistante avancée (APT) **Webworm**, lié à la Chine, a été identifié utilisant une version personnalisée et modifiée de l'outil open-source **SoftEther VPN Bridge** (version 4.44, build 9807). L'objectif principal de cette manipulation est d'échapper à la détection par les outils de sécurité et d'établir un accès distant furtif sans introduire de nouvelles fonctionnalités malveillantes.

**Points clés :**
*   **Masquage :** Le binaire (nommé `netcapa.exe`) est déguisé en logiciel de surveillance réseau sous le nom de "NtMonitor VPN".
*   **Dissimulation du trafic :** Le groupe a remplacé les points de terminaison HTTP par des requêtes d'apparence anodine (`/update/alive.cgi`) et a modifié le protocole de "watermarking" du handshake (passage du format GIF au PNG) pour contourner les signatures de détection existantes.
*   **Modification technique :** Le fichier de configuration est désormais chiffré (en-tête "RCEN") et le composant `hamcore.se2` a été directement intégré à l'exécutable.
*   **Cibles :** Les secteurs gouvernementaux, informatiques et énergétiques en Asie et en Russie.

**Vulnérabilités :**
Aucune CVE spécifique n'est mentionnée, car il s'agit d'une utilisation détournée de logiciel légitime ("dual-use tool"). Le risque repose sur la capacité de l'attaquant à modifier le code source original pour supprimer les empreintes numériques identifiables par les solutions de sécurité.

**Recommandations :**
*   **Analyse comportementale :** Ne pas se fier uniquement aux noms de fichiers ou aux métadonnées des services, mais surveiller les communications réseau sortantes vers des endpoints HTTP suspects.
*   **Filtrage des flux :** Inspecter le contenu du protocole de handshake VPN au sein du réseau pour détecter les incohérences dans les "watermarks" (ex: utilisation inattendue de PNG au lieu de GIF).
*   **Intégrité des binaires :** Vérifier les signatures numériques et l'intégrité des outils d'administration réseau. Un outil comme SoftEther devrait provenir exclusivement des sources officielles et non de répertoires suspects ou renommés.
*   **Surveillance des logs :** Rechercher la présence du fichier de configuration chiffré avec l'en-tête "RCEN" et surveiller les processus utilisant des noms tels que "NtMonitor VPN" qui pourraient trahir une installation non autorisée.

---
[Source](https://thehackernews.com/2026/11/webworm-suspected-of-modifying.html){:target="_blank"}
