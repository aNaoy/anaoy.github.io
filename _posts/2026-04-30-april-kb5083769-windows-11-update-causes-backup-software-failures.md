---
title: 'April KB5083769 Windows 11 update causes backup software failures'
date: 2026-04-30
permalink: /posts/2026/04/30/april-kb5083769-windows-11-update-causes-backup-software-failures/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement des sauvegardes sous Windows 11 suite à la mise à jour KB5083769

La mise à jour de sécurité KB5083769, déployée en avril 2026, entraîne des erreurs critiques dans les logiciels de sauvegarde tiers sur Windows 11 (versions 24H2 et 25H2). Ce problème perturbe le service de clichés instantanés des volumes (VSS) de Microsoft, provoquant des délais d'attente (timeouts) lors de la création de snapshots.

**Points clés :**
*   **Impact opérationnel :** Les logiciels de sauvegarde ne parviennent plus à créer de snapshots, rendant les sauvegardes impossibles.
*   **Logiciels affectés :** De nombreux éditeurs sont touchés, notamment Acronis (Cyber Protect Cloud), Macrium (Reflect), NinjaOne et UrBackup.
*   **Effets secondaires :** Certaines machines peuvent perdre leur connectivité avec les consoles de gestion cloud, apparaissant comme hors ligne.
*   **Vulnérabilité :** Aucune CVE n'est associée à cet incident, il s'agit d'une régression logicielle causée par la mise à jour elle-même.

**Recommandations :**
*   **Contournement temporaire :** Désinstaller la mise à jour KB5083769 via les paramètres système (*Paramètres > Windows Update > Historique des mises à jour > Désinstaller des mises à jour*).
*   **Maintenance :** Suspendre les mises à jour Windows après la désinstallation et redémarrer le système pour restaurer la fonctionnalité VSS.
*   **Veille :** Surveiller les communications officielles de Microsoft pour le déploiement d'un correctif dédié.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/april-kb5083769-windows-11-update-causes-backup-software-failures/){:target="_blank"}
