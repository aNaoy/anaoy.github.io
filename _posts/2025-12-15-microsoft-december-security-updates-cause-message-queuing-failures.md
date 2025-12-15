---
title: 'Microsoft: December security updates cause Message Queuing failures'
date: 2025-12-15
permalink: /posts/2025/12/15/microsoft-december-security-updates-cause-message-queuing-failures/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour de sécurité de décembre : dysfonctionnements de MSMQ sous Windows**

Les mises à jour de sécurité de décembre 2025 pour Windows 10 22H2, Windows Server 2019 et Windows Server 2016, notamment les KB5071546, KB5071544 et KB5071543, entraînent des problèmes avec la fonctionnalité Message Queuing (MSMQ). Les applications d'entreprise et les sites web IIS sont affectés, se manifestant par des files d'attente MSMQ inactives, des erreurs de "ressources insuffisantes" sur les sites IIS, et l'impossibilité pour les applications d'écrire dans les files d'attente. Certains systèmes signalent des erreurs de disque ou de mémoire malgré des ressources suffisantes.

**Points Clés :**

*   **Cause :** Changements apportés au modèle de sécurité de MSMQ, modifiant les permissions sur le dossier `C:\Windows\System32\MSMQ\storage`.
*   **Impact :** Les utilisateurs MSMQ nécessitent désormais des droits d'écriture sur ce dossier, normalement réservé aux administrateurs, provoquant des échecs d'envoi de messages avec des erreurs de ressources. Les environnements MSMQ en cluster sont également touchés lors de fortes charges.
*   **Exception :** Les appareils où les utilisateurs sont connectés avec des privilèges administratifs complets ne sont pas affectés.

**Vulnérabilités :**
Aucune nouvelle vulnérabilité spécifique n'est identifiée dans cet incident, mais l'article mentionne une précédente vulnérabilité critique dans MSMQ (CVE-2023-21554) en avril 2023 qui permettait l'exécution de code à distance.

**Recommandations :**
Microsoft enquête sur le problème et n'a pas fourni de calendrier pour un correctif. En attendant, les administrateurs confrontés à ces dysfonctionnements peuvent envisager de revenir aux mises à jour précédentes, tout en étant conscients des implications de sécurité potentielles.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-december-security-updates-cause-message-queuing-failures/){:target="_blank"}
