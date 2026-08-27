---
title: 'Spark RAT Targets Cambodia, Abuses Vulnerable OPSWAT Driver to Disable Security Tools'
date: 2026-08-27
permalink: /posts/2026/08/27/spark-rat-targets-cambodia-abuses-vulnerable-opswat-driver-to-disable-security-tools/
tags:
- veille-cyber
- hackernews
---
### Campagne de cyberespionnage contre le Cambodge : Utilisation de Spark RAT et de pilotes vulnérables

Une nouvelle campagne d'attaque vise des entités au Cambodge en déployant **Spark RAT**, un cheval de Troie d'accès à distance open source basé sur le langage Go. Les assaillants utilisent des leurres variés (documents gouvernementaux, santé, immobilier) via des e-mails de phishing pour infecter les systèmes.

**Points clés :**
*   **Chaîne d'infection complexe :** L'attaque utilise un installateur *Inno Setup* et une technique de *DLL side-loading* avec un exécutable légitime signé par Tencent.
*   **Technique BYOVD (Bring Your Own Vulnerable Driver) :** Le malware déploie le pilote obsolète `ardrv.sys` (OPSWAT AppRemover) pour élever ses privilèges et neutraliser les logiciels de sécurité.
*   **Dissimulation avancée :** La charge utile est fragmentée dans plusieurs fichiers images PNG, qui sont ensuite décryptés et injectés dans des processus système légitimes comme `vssvc.exe` ou `ctfmon.exe`.
*   **Origine incertaine :** Bien que la campagne présente des similitudes opérationnelles avec le groupe « Silver Fox » (ciblage de logiciels de sécurité chinois, méthodes de persistance), l'absence de preuves matérielles empêche une attribution formelle. Le développement semble néanmoins lié à un environnement sinophone.

**Vulnérabilité exploitée :**
*   **CVE-2026-36425 :** Vulnérabilité présente dans le pilote `ardrv.sys` d'OPSWAT, permettant à l'attaquant d'exécuter du code avec des privilèges élevés pour désactiver les solutions de sécurité (Microsoft Defender, Huorong, Tencent PC Manager).

**Recommandations :**
*   **Mise à jour et durcissement des pilotes :** Auditer les systèmes pour identifier et supprimer les pilotes obsolètes ou vulnérables connus, particulièrement ceux liés à des outils de gestion logicielle.
*   **Surveillance des processus :** Détecter les anomalies d'injection de code dans les processus système critiques (ex: `vssvc.exe`, `ctfmon.exe`) et surveiller l'installation inattendue de services Windows ou de tâches planifiées.
*   **Filtrage des e-mails :** Renforcer les politiques de filtrage des e-mails entrants, en bloquant les archives compressées contenant des exécutables suspects, souvent utilisés comme vecteurs initiaux.
*   **Analyse comportementale :** Déployer des solutions EDR capables de détecter les comportements de type BYOVD et de bloquer le chargement de pilotes non signés ou malveillants.

---
[Source](https://thehackernews.com/2026/08/spark-rat-targets-cambodia-abuses.html){:target="_blank"}
