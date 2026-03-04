---
title: 'Windows 10 KB5075039 update fixes broken Recovery Environment'
date: 2026-03-04
permalink: /posts/2026/03/04/windows-10-kb5075039-update-fixes-broken-recovery-environment/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour de l'environnement de récupération Windows 10 pour corriger un dysfonctionnement**

Une récente mise à jour de Microsoft, référencée KB5075039, vise à résoudre un problème persistant affectant l'environnement de récupération de Windows 10 (WinRE). Cet environnement est essentiel pour le dépannage et la réparation du système d'exploitation en cas de dysfonctionnement, de démarrage impossible, de diagnostics de plantages ou de suppression de logiciels malveillants.

**Points Clés et Vulnérabilités :**

*   **Dysfonctionnement de WinRE suite à une mise à jour antérieure :** La mise à jour KB5068164, déployée en octobre 2025, a introduit un défaut empêchant le bon démarrage de l'environnement de récupération Windows 10.
*   **Problème similaire sur Windows 11 :** Microsoft avait déjà constaté un problème similaire avec les mises à jour de patch Tuesday d'octobre 2025 (KB5066835) sur Windows 11, qui affectait l'utilisation des souris et claviers USB dans l'environnement de récupération. Une correction rapide avait été apportée à ce moment-là.
*   **Nécessité d'une partition WinRE de 256 Mo minimum :** Pour installer la mise à jour corrective KB5075039, la partition dédiée à l'environnement de récupération doit avoir une taille minimale de 256 Mo.

**Recommandations :**

*   **Installer la mise à jour KB5075039 :** Les utilisateurs de Windows 10 confrontés à des problèmes d'accès à l'environnement de récupération doivent installer cette mise à jour.
*   **Vérifier et augmenter la taille de la partition WinRE :** Si la partition WinRE est inférieure à 256 Mo, il est nécessaire de l'agrandir en suivant les instructions fournies par Microsoft (mentionnées dans le texte via un lien vers le support).
*   **Sauvegarder les données avant de redimensionner une partition :** Il est fortement recommandé de sauvegarder toutes les données présentes sur le disque avant de procéder à des modifications sur ses partitions, y compris celle de WinRE.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-10-kb5075039-update-fixes-broken-recovery-environment/){:target="_blank"}
