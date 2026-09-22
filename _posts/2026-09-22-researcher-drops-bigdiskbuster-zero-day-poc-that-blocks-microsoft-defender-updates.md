---
title: 'Researcher Drops BigDiskBuster Zero-Day PoC That Blocks Microsoft Defender Updates'
date: 2026-09-22
permalink: /posts/2026/09/22/researcher-drops-bigdiskbuster-zero-day-poc-that-blocks-microsoft-defender-updates/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité zero-day : BigDiskBuster neutralise les mises à jour de Microsoft Defender

Un chercheur en cybersécurité a publié sur GitHub un outil baptisé **BigDiskBuster**, capable d'empêcher les mises à jour de la plateforme et des signatures de Microsoft Defender. En saturant l'espace disque disponible lors des tentatives de téléchargement, l'outil provoque l'échec systématique de la mise à jour, rendant les définitions de sécurité obsolètes sans pour autant arrêter l'exécution du logiciel.

**Points clés :**
*   **Méthode d'attaque :** L'outil surveille le lecteur système pour détecter le début du téléchargement des mises à jour de Defender, puis crée instantanément un fichier caché occupant tout l'espace libre restant. Il verrouille également le processus `MRT.exe` (outil de suppression des logiciels malveillants) pour empêcher toute mise à jour.
*   **Statut :** Il n'existe actuellement aucun correctif, aucune CVE assignée et aucune communication officielle de Microsoft.
*   **Contexte :** L'outil a été conçu par Abdelhamid Naceri, un ancien chercheur de Microsoft ayant déjà publié plusieurs exploits critiques pour Defender, dont certains ont été activement exploités par des attaquants par le passé.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est disponible à ce jour. Le mécanisme diffère de la vulnérabilité précédente (CVE-2026-45498), ce qui laisse penser que les correctifs actuels ne protègent pas contre cette technique.

**Recommandations :**
*   **Surveillance proactive :** Contrôler régulièrement les versions des signatures et de la plateforme via l'interface Windows Security ou la commande PowerShell `Get-MpComputerStatus`.
*   **Détection d'anomalies :** Surveiller les échecs répétitifs des mises à jour de Defender, les alertes de faible espace disque sur la partition système et la présence de fichiers cachés volumineux dans les répertoires temporaires.
*   **Durcissement :** Restreindre l'exécution de binaires inconnus via des solutions telles que **WDAC** (Windows Defender Application Control) ou **AppLocker** afin de limiter la capacité de l'attaquant à déployer et exécuter ce type d'outil.

---
[Source](https://thehackernews.com/2026/09/researcher-drops-bigdiskbuster-zero-day.html){:target="_blank"}
