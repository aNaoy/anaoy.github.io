---
title: 'Microsoft rolls out new Secure Boot certificates before June expiration'
date: 2026-02-10
permalink: /posts/2026/02/10/microsoft-rolls-out-new-secure-boot-certificates-before-june-expiration/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour des certificats de démarrage sécurisé de Microsoft

Microsoft déploie de nouveaux certificats de démarrage sécurisé (Secure Boot) via les mises à jour mensuelles de Windows. Ces certificats, initialement introduits en 2011, arrivent en fin de vie et expireront fin juin 2026. Le démarrage sécurisé est une fonctionnalité essentielle du firmware UEFI qui garantit le chargement de chargeurs de démarrage fiables, empêchant ainsi l'exécution de logiciels malveillants tels que les rootkits lors du démarrage du système en vérifiant la signature numérique.

Cette initiative représente un effort de maintenance de sécurité coordonné à grande échelle, touchant des millions de configurations d'appareils et de fabricants. Les nouveaux certificats seront installés automatiquement sur les systèmes pris en charge qui reçoivent les mises à jour Windows de Microsoft. Les appareils fabriqués récemment, depuis 2024 pour la plupart, intègrent déjà ces nouveaux certificats.

Cependant, certains appareils plus anciens pourraient nécessiter une mise à jour séparée du firmware de leur fabricant. Microsoft conseille aux utilisateurs de consulter les pages de support de leurs fabricants d'équipement d'origine (OEM) pour s'assurer d'avoir les versions de firmware les plus récentes.

Pour les environnements gérés par des administrateurs informatiques, il est possible de déployer ces certificats via des clés de registre, des paramètres de stratégie de groupe (Group Policy) et le Windows Configuration System (WinCS) pour maintenir les protections du chargeur de démarrage Windows et du démarrage sécurisé.

Les appareils qui ne recevront pas les certificats mis à jour avant la date d'expiration entreront dans un état de sécurité dégradé, avec des protections au niveau du démarrage limitées et une vulnérabilité accrue aux attaques exploitant de nouvelles vulnérabilités.

Microsoft recommande vivement aux utilisateurs de passer à Windows 11, car les versions non prises en charge, comme Windows 10 (hors extensions de sécurité), ne recevront pas ces mises à jour cruciales de certificats. L'utilisation de versions de Windows prises en charge est essentielle pour garantir les meilleures performances et protections.

**Points Clés :**

*   Expiration des certificats de démarrage sécurisé de Microsoft en juin 2026.
*   Déploiement de nouveaux certificats via les mises à jour mensuelles de Windows.
*   Le démarrage sécurisé protège contre les logiciels malveillants au démarrage.
*   Les appareils récents intègrent déjà les nouveaux certificats.
*   Certains appareils plus anciens peuvent nécessiter des mises à jour de firmware spécifiques.
*   Les appareils non mis à jour entreront dans un état de sécurité dégradé.
*   Recommandation de passer à Windows 11 pour bénéficier des mises à jour.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article concernant les certificats eux-mêmes. L'enjeu est l'expiration des certificats existants, qui, une fois expirés, rendront le système vulnérable aux attaques exploitant cette absence de validation.

**Recommandations :**

*   S'assurer que les mises à jour mensuelles de Windows sont appliquées.
*   Pour les appareils plus anciens, vérifier et installer les dernières mises à jour de firmware auprès du fabricant (OEM).
*   Pour les environnements gérés, utiliser les outils d'administration (clés de registre, Group Policy, WinCS) pour déployer les nouveaux certificats.
*   Migrer vers une version de Windows prise en charge, de préférence Windows 11.
*   Maintenir les appareils dans un "état de sécurité élevé" en assurant la mise à jour des certificats avant l'expiration.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-rolls-out-new-secure-boot-certificates-before-june-expiration/){:target="_blank"}
