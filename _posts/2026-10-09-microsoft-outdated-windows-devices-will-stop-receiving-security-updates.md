---
title: 'Microsoft: Outdated Windows devices will stop receiving security updates'
date: 2026-10-09
permalink: /posts/2026/10/09/microsoft-outdated-windows-devices-will-stop-receiving-security-updates/
tags:
- veille-cyber
- bleepingcomp
---
### Fin des mises à jour de sécurité pour les versions obsolètes de Windows

Microsoft a annoncé qu'à partir de 2027, les appareils exécutant des versions non prises en charge de Windows perdront définitivement l'accès aux services Windows Update. Cette interruption est liée au renouvellement des certificats de sécurité utilisés pour valider les mises à jour, dont les dates d'expiration sont fixées aux 17 mai et 19 juin 2027.

**Points clés :**
*   **Expiration des certificats :** Les certificats actuels expireront en mai et juin 2027, rendant les mises à jour impossibles pour les systèmes non mis à jour ou obsolètes.
*   **Impact :** Les systèmes obsolètes ne recevront plus aucun correctif de sécurité, les exposant à des risques critiques.
*   **Exclusion :** Les infrastructures utilisant WSUS (Windows Server Update Services) ne sont pas concernées par cette contrainte directe.
*   **Automatisation :** Les systèmes supportés et maintenus à jour recevront les nouveaux certificats automatiquement via les mises à jour mensuelles.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cette annonce, car il s'agit d'une contrainte technique liée à l'infrastructure de signature. Toutefois, l'absence de mises à jour de sécurité sur des versions obsolètes expose ces systèmes à l'exploitation future de vulnérabilités connues (Zero-day ou non corrigées).

**Recommandations :**
*   **Inventaire :** Identifier immédiatement tous les parcs de machines utilisant des versions de Windows proches de la fin de vie ou obsolètes.
*   **Mises à jour obligatoires :**
    *   *Windows 10/11 et serveurs récents :* Appliquer les correctifs de juillet 2026 (ou ultérieurs) avant juin 2027.
    *   *Windows Server 2016/2019 et 10 LTSC :* Appliquer les correctifs de juillet 2026 (ou ultérieurs) avant mai 2027.
*   **Migration :** Planifier la mise à niveau vers une version de Windows ou de Windows Server actuellement supportée pour tout appareil ne pouvant plus recevoir de mises à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-outdated-windows-devices-will-lose-security-protection-next-year/){:target="_blank"}
