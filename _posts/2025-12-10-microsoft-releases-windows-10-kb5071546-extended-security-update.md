---
title: 'Microsoft releases Windows 10 KB5071546 extended security update'
date: 2025-12-10
permalink: /posts/2025/12/10/microsoft-releases-windows-10-kb5071546-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
## Mise à jour de sécurité Windows 10 KB5071546

Microsoft a déployé la mise à jour de sécurité étendue KB5071546 pour Windows 10, corrigeant 57 vulnérabilités, dont trois failles "zero-day". Cette mise à jour est destinée aux versions Enterprise LTSC et aux utilisateurs inscrits au programme ESU. Elle est appliquée automatiquement et nécessite un redémarrage.

**Points clés :**

*   La mise à jour porte la version de Windows 10 à 19045.6691 et la version Enterprise LTSC 2021 à 19044.6691.
*   Aucune nouvelle fonctionnalité n'est ajoutée ; l'update se concentre sur les correctifs de sécurité et de bugs.

**Vulnérabilités corrigées :**

*   **CVE-2025-54100 :** Une faille de sécurité critique dans PowerShell 5.1 qui permettait l'exécution de code à distance via des scripts malveillants intégrés dans des pages web lors de l'utilisation de la commande `Invoke-WebRequest`.

**Recommandations :**

*   Pour les utilisateurs de Windows 10 Enterprise LTSC ou inscrits au programme ESU, installez la mise à jour KB5071546 via Windows Update.
*   Dans PowerShell 5.1, lors de l'utilisation de la commande `Invoke-WebRequest`, une alerte de sécurité s'affichera désormais pour signaler le risque d'exécution de scripts.
*   Il est recommandé d'utiliser l'argument de ligne de commande `-UseBasicParsing` avec `Invoke-WebRequest` pour éviter l'analyse et l'exécution de scripts contenus dans des pages web potentiellement non fiables.
*   Microsoft ne signale aucun problème connu lié à cette mise à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5071546-extended-security-update/){:target="_blank"}
