---
title: 'Plug and Pwn attack uses fake USB devices for Windows SYSTEM access'
date: 2026-08-12
permalink: /posts/2026/08/12/plug-and-pwn-attack-uses-fake-usb-devices-for-windows-system-access/
tags:
- veille-cyber
- bleepingcomp
---
### Plug and Pwn : L'exploitation des fonctionnalités Plug-and-Play de Windows

La recherche « Plug and Pwn », présentée à la DEF CON 34, met en lumière une méthode d'élévation de privilèges permettant d'obtenir un accès `NT AUTHORITY\SYSTEM` sur Windows en exploitant le mécanisme d'installation automatique des pilotes.

**Points clés :**
* **Mécanisme :** Windows identifie automatiquement les périphériques USB, télécharge des paquets de pilotes signés et exécute les composants logiciels associés (co-installateurs, services) avec les privilèges système les plus élevés.
* **Techniques d'attaque :**
    * **Émulation physique :** Utilisation d'outils comme *FaceDancer* pour usurper l'identité de périphériques légitimes (ex: Sony, Sierra Wireless) et forcer l'installation de logiciels vulnérables.
    * **Attaque distante (NoPlug & Pwn) :** Utilisation de la redirection USB via RDP pour injecter des descripteurs de périphériques contrefaits sans accès physique à la machine cible.
* **Impact :** L'attaque peut être réalisée sans interaction utilisateur, sans session ouverte, et contourne les notifications UAC.

**Vulnérabilités mentionnées :**
* Bien que l'attaque exploite le design même de Windows, certains composants spécifiques ont été identifiés comme vecteurs, notamment le service Atheros (CVE-2019-10617).

**Recommandations :**
* **Désactivation des co-installateurs :** Créer la valeur `DWORD-32` nommée `DisableCoInstallers` (définie à `1`) dans la clé de registre `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Device Installer`.
* **Restrictions de périphériques :** Implémenter des listes blanches d'ID de matériel pour restreindre les périphériques autorisés.
* **Sécurisation RDP :** Désactiver la redirection des périphériques Plug and Play sur les hôtes RDP et VDI sensibles via la politique `fDisablePNPRedir`.

---
[Source](https://www.bleepingcomputer.com/news/security/plug-and-pwn-attack-uses-fake-usb-devices-for-windows-system-access/){:target="_blank"}
