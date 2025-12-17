---
title: 'Microsoft asks admins to reach out for Windows IIS failures fix'
date: 2025-12-17
permalink: /posts/2025/12/17/microsoft-asks-admins-to-reach-out-for-windows-iis-failures-fix/
tags:
- veille-cyber
- bleepingcomp
---
**Échec du Service MSMQ après les Mises à Jour de Décembre**

Une défaillance du service Message Queuing (MSMQ) de Windows, affectant les applications d'entreprise et les sites Internet Information Services (IIS), a été signalée. Ce problème survient après l'installation des mises à jour de sécurité KB5071546, KB5071544 et KB5071543 de décembre 2025. Les environnements d'entreprise sous Windows 10 22H2, Windows Server 2019 et Windows Server 2016 sont principalement concernés.

**Points Clés :**

*   Le service MSMQ, utilisé pour la communication réseau entre applications, est au cœur du problème.
*   Les symptômes incluent l'inactivité des files d'attente MSMQ, l'impossibilité pour les applications d'écrire dans ces files, et des erreurs "ressources insuffisantes" sur les sites IIS.
*   Des messages trompeurs indiquant un manque d'espace disque ou de mémoire peuvent apparaître, même si les ressources sont suffisantes.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifique, mais il attribue le problème à des modifications du modèle de sécurité MSMQ.

**Recommandations :**

*   Les entreprises affectées sont invitées à contacter le support Microsoft pour entreprises afin d'obtenir une solution de contournement temporaire.
*   Une réversion des mises à jour de sécurité peut être envisagée.
*   Les utilisateurs de Windows Home ou Pro sur des appareils personnels sont peu susceptibles d'être affectés.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-asks-it-admins-to-reach-out-for-windows-iis-failures-fix/){:target="_blank"}
