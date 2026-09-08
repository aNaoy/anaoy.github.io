---
title: 'Microsoft: Windows Server 2025 changes causing app crashes'
date: 2026-09-08
permalink: /posts/2026/09/08/microsoft-windows-server-2025-changes-causing-app-crashes/
tags:
- veille-cyber
- bleepingcomp
---
### Instabilité des applications sur Windows Server 2025 : Conflits de gestion mémoire

Une modification récente de la gestion de la mémoire dans Windows Server 2025 provoque des plantages et des corruptions de données pour certaines applications critiques. Ce problème touche spécifiquement les logiciels utilisant les *Address Windowing Extensions* (AWE), notamment SQL Server lorsque la stratégie « Verrouiller les pages en mémoire » (LPIM) est activée.

**Points clés :**
* **Impact :** Violations d'accès (erreur 0xC0000005), corruption de mémoire, arrêts inopinés des services SQL Server et échecs lors des opérations de maintenance (ex: DBCC CHECKDB).
* **Cause :** Incompatibilité entre les nouvelles méthodes de gestion mémoire du système d'exploitation et les comportements hérités des applications utilisant AWE/LPIM.
* **Vulnérabilité :** Aucune CVE associée (problème de stabilité logicielle/conception).

**Recommandations :**
* **Contournement temporaire :** Désactiver la stratégie « Verrouiller les pages en mémoire » (LPIM) pour le compte de service SQL Server. Pour les autres applications utilisant AWE, vérifier s'il est possible de désactiver cette fonctionnalité.
* **Avertissement :** La désactivation de LPIM peut impacter les performances et la gestion mémoire de SQL Server ; une évaluation préalable dans un environnement de test est recommandée.
* **Suivi :** Surveiller les prochaines mises à jour de Windows Server 2025 pour l'application d'un correctif définitif.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-server-2025-changes-may-cause-app-crashes/){:target="_blank"}
