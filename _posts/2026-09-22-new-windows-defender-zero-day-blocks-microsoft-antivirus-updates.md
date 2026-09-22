---
title: 'New Windows Defender zero-day blocks Microsoft antivirus updates'
date: 2026-09-22
permalink: /posts/2026/09/22/new-windows-defender-zero-day-blocks-microsoft-antivirus-updates/
tags:
- veille-cyber
- bleepingcomp
---
### Nouvelle faille zero-day dans Microsoft Defender : BigDiskBuster

Un chercheur en sécurité nommé Abdelhamid Naceri a publié un nouvel exploit zero-day baptisé **BigDiskBuster**, capable de bloquer les mises à jour de Microsoft Defender.

**Points clés :**
* **Fonctionnement :** L'outil doit être exécuté en arrière-plan pour empêcher le téléchargement des mises à jour de plateforme et de signatures, laissant le système vulnérable avec une version obsolète.
* **Compatibilité :** L'exploit affecte toutes les versions de Windows actuellement prises en charge.
* **Contexte :** Cette divulgation s'inscrit dans une série d'attaques menées par le chercheur (ancien employé Microsoft) en raison d'un litige personnel avec l'entreprise.
* **Historique récent :** Le chercheur est également à l'origine d'autres vulnérabilités récentes telles que *ShieldCrash* (élévation de privilèges SYSTEM) et *ShieldBreak* (CVE-2026-69414).

**Vulnérabilités identifiées :**
* **BigDiskBuster :** Deni de service sur les mises à jour (non patché).
* **ShieldCrash :** Élévation de privilèges (non patché).
* **ShieldBreak (CVE-2026-69414) :** Élévation de privilèges (patché).
* **RoguePlanet :** Élévation de privilèges (patché).

**Recommandations :**
* Étant donné l'absence de correctif officiel pour BigDiskBuster, il est conseillé de surveiller l'état de mise à jour de Microsoft Defender sur les postes de travail.
* Appliquer rigoureusement les mises à jour de sécurité cumulatives diffusées lors du "Patch Tuesday".
* Maintenir une vigilance accrue sur les outils de télémétrie et de gestion des vulnérabilités pour détecter toute activité anormale bloquant les services de sécurité natifs de Windows.

---
[Source](https://www.bleepingcomputer.com/news/security/new-windows-defender-zero-day-blocks-microsoft-antivirus-updates/){:target="_blank"}
