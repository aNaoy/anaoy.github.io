---
title: 'EDR killer tool uses signed kernel driver from forensic software'
date: 2026-02-05
permalink: /posts/2026/02/05/edr-killer-tool-uses-signed-kernel-driver-from-forensic-software/
tags:
- veille-cyber
- bleepingcomp
---
**Outil d'élimination d'EDR exploitant un pilote noyau légitime mais obsolète**

Une technique malveillante a été observée utilisant un ancien pilote noyau du logiciel d'investigation forensique EnCase pour désactiver les solutions de sécurité Endpoint Detection and Response (EDR). Cet outil d'élimination cible 59 produits de sécurité différents, les rendant inopérants.

L'attaque démarre par l'exploitation de vulnérabilités dans les identifiants VPN SonicWall et l'absence d'authentification multifacteur (MFA), permettant aux acteurs malveillants d'accéder au réseau. Ils procèdent ensuite à une reconnaissance interne agressive avant de déployer l'outil d'élimination.

Ce dernier, un exécutable 64 bits, utilise le pilote 'EnPortv.sys'. Bien que le certificat de ce pilote soit expiré et révoqué depuis 2010, Windows l'accepte toujours car le système de vérification de signature de pilote ne contrôle pas les listes de révocation de certificats (CRL) et autorise les certificats émis avant juillet 2015. Le pilote est installé comme un service matériel OEM, assurant une persistance même après un redémarrage. Il utilise l'interface IOCTL du pilote pour terminer les processus de sécurité, contournant même des protections comme Protected Process Light (PPL). Le processus de suppression des services de sécurité s'exécute en continu, réactivant immédiatement tout service redémarré.

Les chercheurs suspectent un lien avec des activités de ransomware, bien que l'attaque ait été interrompue avant le déploiement de la charge utile finale.

**Points Clés :**

*   Utilisation d'un pilote noyau légitime mais obsolète (EnCase) pour contourner les défenses.
*   Ciblage de 59 outils de sécurité EDR et antivirus.
*   Obtention d'une persistance via l'installation du pilote comme service matériel.
*   Exploitation de l'absence de vérification des CRL par Windows pour les anciens certificats de pilotes signés.
*   Possibilité de contourner des protections comme Protected Process Light (PPL).

**Vulnérabilités :**

*   La technique "Bring Your Own Vulnerable Driver" (BYOVD) reste efficace contre les systèmes Windows.
*   L'absence de vérification des listes de révocation de certificats (CRL) par le mécanisme de signature de pilote de Windows pour les certificats plus anciens.
*   L'exception pour les certificats émis avant le 29 juillet 2015 dans Windows 10 version 1607, permettant l'exécution de pilotes non sécurisés.

**Recommandations :**

*   Activer l'authentification multifacteur (MFA) sur tous les services d'accès à distance.
*   Surveiller les journaux VPN pour détecter les activités suspectes.
*   Activer l'intégrité de la mémoire (HVCI) pour appliquer la liste de blocage des pilotes vulnérables de Microsoft.
*   Surveiller l'installation de services noyau se faisant passer pour des composants matériels ou OEM.
*   Déployer les règles WDAC (Windows Defender Application Control) et ASR (Attack Surface Reduction) pour bloquer les pilotes signés vulnérables.

---
[Source](https://www.bleepingcomputer.com/news/security/edr-killer-tool-uses-signed-kernel-driver-from-forensic-software/){:target="_blank"}
