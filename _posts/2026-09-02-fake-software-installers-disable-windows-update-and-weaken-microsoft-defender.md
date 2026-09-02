---
title: 'Fake Software Installers Disable Windows Update and Weaken Microsoft Defender'
date: 2026-09-02
permalink: /posts/2026/09/02/fake-software-installers-disable-windows-update-and-weaken-microsoft-defender/
tags:
- veille-cyber
- hackernews
---
### Campagne de malwares « Silver Fox » : Distribution de logiciels contrefaits

Une campagne active, attribuée au groupe de menace chinois « Silver Fox » (ou Yinhu), cible des utilisateurs cherchant à télécharger des logiciels populaires. Les attaquants utilisent des sites web miroirs, visuellement identiques aux sites officiels, pour distribuer des installateurs malveillants générés dynamiquement.

**Points clés :**
* **Vecteur d'attaque :** Sites web factices (.com.cn et .hl.cn) incitant au téléchargement d'archives ZIP contenant des installateurs malveillants.
* **Persistance et Évasion :** Utilisation de tâches planifiées masquées, modification des permissions (DACL) via `icacls` pour empêcher la suppression des fichiers, et désactivation ciblée de Microsoft Defender via PowerShell.
* **Neutralisation des mises à jour :** Le malware sabote Windows Update en arrêtant des services critiques (`wuauserv`, `UsoSvc`, `WaaSMedicSvc`) et en supprimant le cache `SoftwareDistribution`.
* **Cibles :** Secteurs variés (santé, industrie, gouvernement, éducation) avec une forte concentration sur des organisations ayant des opérations en Chine.
* **Charges utiles :** Déploiement de backdoors sophistiqués comme **ValleyRAT** (via détournement de DLL) ou **Gh0st RAT**, permettant l'espionnage, le vol de données (keylogger, presse-papier) et le contrôle à distance.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur l'ingénierie sociale (domaines contrefaits) et l'abus de fonctionnalités légitimes de Windows (DLL Sideloading, services `msiexec.exe`, désactivation via PowerShell).

**Recommandations :**
* **Vérification des sources :** Ne télécharger des logiciels que depuis les sites officiels et vérifier systématiquement l'URL avant toute action.
* **Surveillance des tâches planifiées :** Auditer régulièrement les tâches planifiées pour détecter des noms ou des comportements suspects.
* **Intégrité du système :** Surveiller l'état des services de mise à jour Windows (`wuauserv`) et les exclusions de Microsoft Defender.
* **Politiques de sécurité :** Restreindre les privilèges des utilisateurs pour limiter la capacité des scripts (PowerShell) à modifier les autorisations de fichiers (`icacls`) ou à manipuler les services système.
* **Utilisation d'outils EDR :** Maintenir des solutions de détection et de réponse (EDR) activées pour bloquer les comportements anormaux, comme ceux détectés par Microsoft via l'« attack disruption ».

---
[Source](https://thehackernews.com/2026/09/fake-software-installers-disable.html){:target="_blank"}
