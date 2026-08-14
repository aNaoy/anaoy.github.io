---
title: 'APT group HoneyMyte upgrades CoolClient: the backdoor gets a kernel-level Windows rootkit'
date: 2026-08-14
permalink: /posts/2026/08/14/apt-group-honeymyte-upgrades-coolclient-the-backdoor-gets-a-kernel-level-windows-rootkit/
tags:
- veille-cyber
- securelist
---
### Évolution du backdoor CoolClient : Intégration d'un rootkit noyau par HoneyMyte

Le groupe APT HoneyMyte (aussi connu sous le nom de Mustang Panda) a considérablement renforcé son backdoor **CoolClient** en y intégrant un pilote (driver) en mode noyau. Utilisé principalement pour l'espionnage dans des pays asiatiques (Birmanie, Mongolie, Pakistan), ce malware s'appuie désormais sur des capacités de rootkit pour dissimuler ses activités et persister sur les systèmes infectés.

#### Points clés
*   **Chaîne d'infection :** L'intrusion initiale est généralement réalisée via le malware *PlugX*. CoolClient est ensuite déployé en tant que backdoor secondaire via une technique de *DLL sideloading* (détournement d'une application légitime, souvent renommée `defender.exe`).
*   **Rootkit noyau (`msagent.sys`) :** Le malware déploie un pilote signé numériquement. Il communique avec celui-ci via des requêtes IOCTL pour protéger ses fichiers, ses clés de registre et son propre processus.
*   **Capacités de dissimulation :**
    *   **Processus :** Dissimulation dans la liste active des processus Windows et protection contre l'arrêt via des callbacks noyau.
    *   **Réseau :** Filtrage du driver `Nsiproxy` pour masquer les connexions vers les serveurs de commande et contrôle (C2).
    *   **Persistance :** Utilisation de tâches planifiées, d'entrées AutoRun et d'une installation en tant que service Windows (`media_updaten`).
*   **Évasion :** Utilisation avancée de techniques de contournement de l'UAC (User Account Control) via des appels RPC et de la falsification de processus parent (PPID spoofing) pour s'exécuter avec des privilèges élevés sous une apparence légitime.

#### Vulnérabilités exploitées
Bien qu'aucune CVE spécifique ne soit mentionnée, le malware exploite des comportements natifs de Windows et des failles de conception pour maintenir sa furtivité :
*   **DLL Sideloading :** Exploitation du chargement de bibliothèques par des exécutables légitimes.
*   **Manipulation de l'UAC :** Abus des interfaces RPC pour élever les privilèges sans déclencher d'alertes visuelles.
*   **Hooks noyau :** Détournement de callbacks système (`PsSetCreateProcessNotifyRoutineEx`, `CmRegisterCallbackEx`) pour masquer la présence du malware.

#### Recommandations de défense
1.  **Surveillance des exclusions :** Auditer les configurations de Microsoft Defender pour détecter l'ajout suspect d'exclusions sur les répertoires systèmes (`wmic ... Add ExclusionPath`).
2.  **Analyse des services :** Surveiller la création de nouveaux services Windows, particulièrement ceux utilisant des noms trompeurs imitant des composants de sécurité (`media_updaten`, `msagent`).
3.  **Surveillance des processus :** Détecter le chargement de pilotes (drivers) non signés ou signés par des certificats obsolètes, ainsi que les comportements anormaux des processus système (ex: `synchost.exe` injecté).
4.  **Audit EDR :** Configurer les outils de détection pour identifier les appels IOCTL suspects et l'utilisation de techniques de *PPID spoofing* ou de manipulation de la liste des processus (`ActiveProcessLinks`).
5.  **Analyse réseau :** Surveiller les communications vers des adresses IP non habituelles, même si le pilote tente de filtrer les informations via le driver `Nsiproxy`.

---
[Source](https://securelist.com/honeymyte-coolclient-driver-rootkit/121028/){:target="_blank"}
