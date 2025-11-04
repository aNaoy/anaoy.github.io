---
title: 'Windows 10 update bug triggers incorrect end-of-support alerts'
date: 2025-11-04
permalink: /posts/2025/11/04/windows-10-update-bug-triggers-incorrect-end-of-support-alerts/
tags:
- veille-cyber
- bleepingcomp
---
**Bug d'alerte de fin de support sur Windows 10**

Des utilisateurs de Windows 10 ont constaté l'affichage de messages d'alerte incorrects indiquant que leur version a atteint la fin du support, alors qu'elle est toujours activement supportée, notamment pour les éditions Enterprise LTSC 2021 et IoT Enterprise LTSC 2021, ainsi que pour les versions 22H2 bénéficiant du programme de mises à jour de sécurité étendues (ESU). Ce dysfonctionnement, apparu suite aux mises à jour d'octobre 2025, est d'ordre cosmétique et n'affecte pas la réception des correctifs de sécurité.

**Points Clés :**

*   Des notifications erronées de fin de support s'affichent sur certaines versions de Windows 10.
*   Les systèmes concernés incluent Windows 10 Enterprise LTSC 2021, Windows 10 IoT Enterprise LTSC 2021, et les versions 22H2 sous ESU.
*   Malgré l'alerte, les appareils continueront de recevoir les mises à jour de sécurité.
*   Microsoft a déployé une correction automatique via une mise à jour de configuration cloud.

**Vulnérabilités :**

*   Aucune vulnérabilité de sécurité n'est décrite dans l'article. L'incident concerne une erreur d'affichage.

**Recommandations :**

*   Pour les environnements gérés par des administrateurs, une politique de groupe via le "Known Issue Rollback" (KIR) peut être appliquée pour désactiver le message erroné, en configurant la valeur KB5066791 251020_20401 sur "Disabled". Des instructions sont disponibles sur le site de support Microsoft.
*   Microsoft prévoit d'intégrer une correction définitive dans une future mise à jour de Windows.
*   Les utilisateurs souhaitant prolonger le support de Windows 10 après sa date officielle de fin (14 octobre) peuvent souscrire au programme ESU, dont les tarifs varient selon le type d'utilisateur (domestique, entreprise). Des options gratuites existent pour certains utilisateurs (Microsoft Rewards, EEA).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-10-update-bug-triggers-incorrect-end-of-support-alerts/){:target="_blank"}
