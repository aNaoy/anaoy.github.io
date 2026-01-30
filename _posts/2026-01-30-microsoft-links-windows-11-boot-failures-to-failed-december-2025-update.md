---
title: 'Microsoft links Windows 11 boot failures to failed December 2025 update'
date: 2026-01-30
permalink: /posts/2026/01/30/microsoft-links-windows-11-boot-failures-to-failed-december-2025-update/
tags:
- veille-cyber
- bleepingcomp
---
**Échec de démarrage de Windows 11 lié à des mises à jour antérieures**

Des problèmes de démarrage sous Windows 11, survenant après l'installation des mises à jour de janvier 2026 (notamment KB5074109), ont été identifiés comme étant la conséquence de tentatives précédentes infructueuses d'installation de la mise à jour de sécurité de décembre 2025. Ces échecs ont laissé les systèmes dans un état instable.

**Points Clés :**

*   Les échecs de démarrage se manifestent par un écran de BSOD (Blue Screen of Death) avec l'erreur "UNMOUNTABLE_BOOT_VOLUME".
*   L'origine du problème est un état "impropre" du système résultant de l'échec et du retrait de la mise à jour de décembre 2025.
*   Tenter d'installer de nouvelles mises à jour dans cet état peut empêcher le système de démarrer.
*   Microsoft travaille à une solution partielle pour éviter que de nouveaux appareils n'entrent dans cet état de non-démarrage lors d'une tentative de mise à jour.
*   Cette solution partielle ne corrigera pas les appareils déjà affectés ni n'empêchera l'état initial problématique de survenir.
*   Le problème semble actuellement limité aux appareils physiques et n'affecte pas les machines virtuelles.

**Vulnérabilités :**

Aucun CVE spécifique n'est mentionné dans l'article. L'incident est décrit comme une instabilité logicielle suite à un échec de mise à jour.

**Recommandations :**

*   Pour les utilisateurs rencontrant des problèmes de démarrage, une solution de réparation pourrait être nécessaire.
*   Pour les systèmes dont la mise à jour de décembre 2025 a échoué, une attention particulière est requise avant d'appliquer de futures mises à jour. Microsoft enquête sur les causes de ces échecs initiaux.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-links-windows-11-boot-failures-to-failed-december-2025-update/){:target="_blank"}
