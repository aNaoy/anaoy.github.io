---
title: 'RIP RegPwn'
date: 2026-03-13
permalink: /posts/2026/03/13/rip-regpwn/
tags:
- veille-cyber
- zerodaysfans
---
### RegPwn : Élévation de privilèges via les fonctionnalités d'accessibilité Windows

**RegPwn** est une vulnérabilité d'élévation de privilèges permettant à un utilisateur standard d'obtenir des droits **SYSTEM** sur Windows 10, 11 et les versions Server (2012 à 2025). Elle repose sur une faille dans la gestion des configurations des outils d'accessibilité par le processus `atbroker.exe`.

#### Points clés
* **Mécanisme :** Le système copie des configurations d'accessibilité depuis des clés de registre utilisateur (`HKCU`) vers des emplacements `HKLM` lors de l'interaction avec le Bureau Sécurisé (Secure Desktop).
* **Vecteur d'attaque :** Un attaquant peut remplacer la clé de destination `HKLM` par un lien symbolique de registre juste avant que le processus `osk.exe` (s'exécutant en tant que SYSTEM) ne tente d'y écrire.
* **Exploitation :** L'utilisation de verrous opportunistes (oplocks) sur un fichier spécifique permet de gagner la fenêtre de tir nécessaire pour détourner l'écriture vers une clé arbitraire, comme celle d'un service système (`ImagePath`), afin de provoquer une exécution de code malveillant.

#### Vulnérabilités
* **CVE-2026-24291 :** Vulnérabilité d'élévation de privilèges (EoP) liée à une gestion non sécurisée des liens symboliques dans les clés de registre des fonctionnalités d'accessibilité.

#### Recommandations
* **Mise à jour :** Appliquer les correctifs du « Patch Tuesday » de mars 2026 diffusés par Microsoft pour corriger cette vulnérabilité.
* **Surveillance :** Surveiller les tentatives anormales de création de liens symboliques de registre ou les modifications inattendues des clés `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Accessibility\`.

---
[Source](https://www.mdsec.co.uk/2026/03/rip-regpwn/){:target="_blank"}
