---
title: 'Microsoft releases emergency updates to fix Windows recovery'
date: 2025-08-20
permalink: /posts/2025/08/20/microsoft-releases-emergency-updates-to-fix-windows-recovery/
tags:
- veille-cyber
- bleepingcomp
---
### Mises à jour urgentes de Microsoft pour corriger les problèmes de récupération Windows

Microsoft a déployé des mises à jour d'urgence (hors bande) pour résoudre un problème connu qui empêchait les opérations de réinitialisation et de récupération de Windows après l'installation des mises à jour de sécurité d'août 2025. Ces problèmes affectent les systèmes exécutant Windows 10 et certaines versions de Windows 11.

**Points clés :**

*   Les mises à jour de sécurité d'août 2025 (KB5063875 pour Windows 11, KB5063709 et KB5063877 pour Windows 10) ont introduit un bug.
*   Ce bug empêche le bon fonctionnement des fonctions "Réinitialiser ce PC" (en conservant les fichiers) et "Résoudre les problèmes via Windows Update".
*   Les professionnels de l'informatique peuvent également être affectés lors de la réinitialisation à distance des appareils via le fournisseur de services de configuration RemoteWipe (RemoteWipe CSP).

**Mises à jour concernées par le bug (août 2025) :**

*   KB5063875 (Windows 11, versions 23H2 et 22H2)
*   KB5063709 (Windows 10 22H2, Windows 10 Enterprise LTSC 2021, Windows 10 IoT Enterprise LTSC 2021)
*   KB5063877 (Windows 10 Enterprise LTSC 2019, Windows 10 IoT Enterprise LTSC 2019)

**Mises à jour d'urgence publiées pour corriger le problème :**

*   KB5066189 (Windows 11, versions 23H2 et 22H2)
*   KB5066188 (Windows 10 22H2, Windows 10 Enterprise LTSC 2021, Windows 10 IoT Enterprise LTSC 2021)
*   KB5066187 (Windows 10 Enterprise LTSC 2019, Windows 10 IoT Enterprise LTSC 2019)

**Recommandations :**

*   Si vous n'avez pas encore installé les mises à jour de sécurité d'août 2025, installez de préférence les mises à jour d'urgence hors bande mentionnées ci-dessus.
*   Si votre système n'est pas affecté par ce problème, l'installation de ces mises à jour d'urgence n'est pas nécessaire.
*   Ces mises à jour correctives sont disponibles via Windows Update, Windows Update for Business, ou peuvent être téléchargées manuellement depuis le catalogue Microsoft Update.

L'article mentionne également d'autres corrections récentes concernant des échecs de mise à jour à partir de partages réseau et des erreurs (0x80240069) sur Windows 11 24H2.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques pour ce problème de réinitialisation/récupération. Il s'agit d'un bug fonctionnel plutôt que d'une vulnérabilité de sécurité exploitée par des attaquants.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-emergency-updates-to-fix-windows-recovery/){:target="_blank"}
