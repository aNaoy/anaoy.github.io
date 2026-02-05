---
title: 'Malicious Script Delivering More Maliciousness, (Wed, Feb 4th)'
date: 2026-02-05
permalink: /posts/2026/02/05/malicious-script-delivering-more-maliciousness-wed-feb-4th/
tags:
- veille-cyber
- sans-isc
---
### Un script malveillant délivre un logiciel malveillant sophistiqué

Une campagne d'hameçonnage récente utilise un script malveillant pour livrer une charge utile complexe, culminant avec le logiciel malveillant XWorm. Le processus commence par un fichier `.bat` qui, au lieu d'exécuter sa fonction prévue, appelle une routine cachée. Cette routine obfusque et décode ensuite une charge utile via PowerShell.

La charge utile initiale récupère une image PNG à partir d'un serveur distant. Cependant, cette image contient des données supplémentaires encodées en Base64, délimitées par des balises spécifiques. Ces données constituent un shellcode qui, une fois décodé (via un script Python spécifique), révèle un programme .NET.

Ce programme .NET est conçu pour établir la persistance sur le système compromis en créant une tâche planifiée. Il communique ensuite avec un serveur de commande et contrôle (C2) via l'API Telegram, envoyant des informations sur le système telles que le nom d'utilisateur, le système d'exploitation, les détails du processeur et de la RAM. Le logiciel malveillant découvert est identifié comme XWorm, une version récente de ce trojan d'accès à distance.

**Points clés :**

*   Utilisation d'un script `.bat` modifié pour exécuter une charge utile cachée.
*   Obfuscation et décodage d'une charge utile via PowerShell.
*   Stockage de données malveillantes dans une image PNG.
*   Décodage d'un shellcode à l'aide d'un script Python dédié.
*   Déploiement d'un programme .NET.
*   Établissement de la persistance via des tâches planifiées.
*   Utilisation de Telegram comme canal de commande et contrôle (C2).
*   Identification du logiciel malveillant comme une variante de XWorm.

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique (CVE) n'est explicitement mentionnée dans le processus de livraison ou l'exploitation de ces charges utiles. L'attaque repose sur la confiance de l'utilisateur et l'exécution de scripts malveillants.

**Recommandations :**

*   **Vigilance accrue face aux e-mails suspects :** Soyez prudent avec les pièces jointes et les liens provenant de sources inconnues ou inattendues.
*   **Analyse approfondie des scripts :** Les administrateurs système et les analystes de sécurité devraient examiner attentivement les scripts d'apparence légitime, en particulier ceux provenant de sources non fiables ou présentant des comportements inhabituels.
*   **Solutions de sécurité à jour :** Maintenir les logiciels antivirus, anti-malwares et autres solutions de sécurité à jour.
*   **Surveillance des tâches planifiées :** Surveiller régulièrement les tâches planifiées sur les systèmes pour détecter toute activité suspecte.
*   **Restrictions sur l'exécution de PowerShell :** Mettre en place des politiques pour restreindre l'exécution de scripts PowerShell potentiellement malveillants.
*   **Segmentation du réseau :** Isoler les systèmes critiques pour limiter la propagation potentielle en cas d'infection.

---
[Source](https://isc.sans.edu/diary/rss/32682){:target="_blank"}
