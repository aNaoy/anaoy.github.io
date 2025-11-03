---
title: 'Microsoft: Patch for WSUS flaw disabled Windows Server hotpatching'
date: 2025-11-03
permalink: /posts/2025/11/03/microsoft-patch-for-wsus-flaw-disabled-windows-server-hotpatching/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour WSUS : Corriger une faille et résoudre un effet secondaire**

Une mise à jour d'urgence pour corriger une faille de sécurité critique dans le service de mise à jour Windows Server (WSUS) a entraîné un problème inattendu sur certains systèmes Windows Server 2025.

**Points clés :**

*   La vulnérabilité **CVE-2025-59287** de WSUS a été exploitée activement.
*   Une mise à jour hors bande (KB5070881) a été publiée pour y remédier.
*   Cette mise à jour a eu pour effet de désactiver la fonction "Hotpatching" sur les serveurs Windows Server 2025 inscrits à ce programme.
*   Microsoft a cessé de proposer KB5070881 aux systèmes affectés et ceux qui l'ont installée ne recevront plus de mises à jour "Hotpatch" en novembre et décembre.
*   Ces systèmes recevront à la place les mises à jour de sécurité mensuelles classiques, nécessitant un redémarrage, et seront réintégrés au programme "Hotpatch" en janvier 2026.
*   Une nouvelle mise à jour de sécurité (KB5070893) a été publiée pour corriger la faille CVE-2025-59287 sans affecter le "Hotpatching".

**Vulnérabilités :**

*   **CVE-2025-59287** : Vulnérabilité d'exécution de code à distance (RCE) dans WSUS.

**Recommandations :**

*   Les administrateurs ayant téléchargé KB5070881 mais ne l'ayant pas encore déployé doivent installer KB5070893 via les paramètres Windows Update.
*   Les machines ayant déjà installé KB5070881 devront attendre les mises à jour régulières et la réintégration du programme "Hotpatch" en janvier 2026.
*   Microsoft a désactivé l'affichage des détails des erreurs de synchronisation dans le rapport d'erreurs WSUS pour pallier la vulnérabilité CVE-2025-59287.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-patch-for-wsus-flaw-disabled-windows-server-hotpatching/){:target="_blank"}
