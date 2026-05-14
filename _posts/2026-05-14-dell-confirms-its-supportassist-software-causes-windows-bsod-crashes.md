---
title: 'Dell confirms its SupportAssist software causes Windows BSOD crashes'
date: 2026-05-14
permalink: /posts/2026/05/14/dell-confirms-its-supportassist-software-causes-windows-bsod-crashes/
tags:
- veille-cyber
- bleepingcomp
---
### Instabilité critique des systèmes Dell suite à une mise à jour logicielle

Dell a confirmé qu'une mise à jour récente de son logiciel *SupportAssist Remediation* (version 5.5.16.0) provoque des écrans bleus de la mort (BSOD) sur de nombreux systèmes Windows 10 et 11. Cette défaillance logicielle génère une erreur critique de type `0xEF_DellSupportAss_BUGCHECK_CRITICAL_PROCESS`, entraînant des redémarrages intempestifs.

**Points clés :**
*   **Cause identifiée :** La version 5.5.16.0 du service *Dell SupportAssist Remediation* ou *Alienware SupportAssist Remediation*.
*   **Impact :** Instabilité du système, plantages récurrents et impossibilité d'utiliser normalement l'ordinateur.
*   **Historique :** Ce problème s'ajoute à une série d'incidents récents liés aux mises à jour Dell (BIOS, versions précédentes de SupportAssist), soulignant une fragilité récurrente dans les outils de gestion du constructeur.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cet incident de plantage actuel.
*   *Note historique :* L'article rappelle que le service SupportAssist a déjà été exposé par le passé à des vulnérabilités critiques dans sa fonctionnalité *BIOSConnect*, permettant à des attaquants distants d'exécuter du code au niveau du BIOS.

**Recommandations :**
*   **Désinstallation :** Supprimer le service *Dell SupportAssist Remediation* ou *Alienware SupportAssist Remediation* via le menu "Applications installées" des paramètres Windows.
*   **Attention :** La suppression de ce service rendra les points de restauration créés par *Dell OS SupportAssist Recovery* indisponibles.
*   **Support :** Pour les utilisateurs rencontrant toujours des BSOD après la désinstallation, il est conseillé de contacter directement le support technique de Dell.

---
[Source](https://www.bleepingcomputer.com/news/software/dell-confirms-its-supportassist-software-causes-windows-bsod-crashes/){:target="_blank"}
