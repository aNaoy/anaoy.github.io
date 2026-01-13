---
title: 'Microsoft releases Windows 10 KB5073724 extended security update'
date: 2026-01-13
permalink: /posts/2026/01/13/microsoft-releases-windows-10-kb5073724-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour de Sécurité Windows 10 KB5073724 : Corrections et Prévention**

Microsoft a déployé la mise à jour KB5073724 pour Windows 10, axée exclusivement sur la correction de failles de sécurité et de bugs, notamment ceux introduits par des mises à jour précédentes. Cette mise à jour est disponible pour les utilisateurs de Windows 10 Enterprise LTSC et ceux inscrits au programme ESU, via le mécanisme habituel de Windows Update. Elle élève la version des systèmes concernés à 19045.6809 (ou 19044.6809 pour LTSC 2021).

**Points Clés :**

*   **Corrections de Sécurité :** La mise à jour traite 114 vulnérabilités, incluant trois failles "zero-day" exploitées activement.
*   **Suppression de Pilotes :** Des pilotes de modem Agere (agrsm64.sys, agrsm.sys, smserl64.sys, smserial.sys) ont été supprimés. L'utilisation de matériel modem dépendant de ces pilotes ne sera plus prise en charge sur Windows.
*   **Expiration des Certificats Secure Boot :** Un problème critique lié à l'expiration prochaine de plusieurs certificats Secure Boot en 2026 a été résolu. Ces certificats sont essentiels pour la validation des composants de démarrage de Windows, des chargeurs de démarrage tiers et des mises à jour de révocation Secure Boot. Sans ces mises à jour, les protections Secure Boot pourraient être compromise, permettant potentiellement à des acteurs malveillants de contourner les mesures de sécurité.
*   **Mise à Jour ciblée des Certificats :** Microsoft déploie de nouveaux certificats Secure Boot via des mises à jour ciblées, assurant une distribution progressive et sécurisée.
*   **Correction pour WinSqlite3.dll :** Un composant de base de Windows, WinSqlite3.dll, a été mis à jour pour corriger une détection erronée de vulnérabilité par certains logiciels de sécurité.

**Vulnérabilités :**

*   Vulnérabilité d'élévation de privilèges dans les pilotes de modem Agere (CVE non spécifié dans l'article).
*   Une faille de sécurité dans la DLL tierce WinSqlite3.dll (CVE non spécifié dans l'article).
*   Expiration de certificats Secure Boot (les CVE spécifiques aux certificats eux-mêmes ne sont pas mentionnés, mais l'impact est sur la chaîne de confiance de démarrage sécurisé).

**Recommandations :**

*   Les utilisateurs de Windows 10 Enterprise LTSC et du programme ESU doivent installer la mise à jour KB5073724 via Windows Update.
*   Il est crucial de s'assurer que les systèmes reçoivent cette mise à jour pour garantir la continuité des protections Secure Boot après l'expiration des certificats en 2026.
*   Les utilisateurs de matériel modem dépendant des pilotes Agere devront envisager des alternatives après cette mise à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5073724-extended-security-update/){:target="_blank"}
