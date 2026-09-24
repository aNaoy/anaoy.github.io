---
title: 'Microsoft fixes bug that broke Windows File History backup feature'
date: 2026-09-24
permalink: /posts/2026/09/24/microsoft-fixes-bug-that-broke-windows-file-history-backup-feature/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif de Microsoft pour la fonctionnalité « Historique des fichiers » sous Windows

Suite aux mises à jour de sécurité de septembre 2026, de nombreux utilisateurs Windows ont rencontré des dysfonctionnements majeurs avec la fonctionnalité « Historique des fichiers ». Ce bug empêche la sauvegarde automatique des données vers des disques externes ou des emplacements réseau, rendant parfois impossible la restauration de versions antérieures de documents.

**Points clés :**
* **Dysfonctionnement :** L'outil de sauvegarde génère des erreurs système (via `FileHistory.exe` et `KERNELBASE.dll`), affiche des demandes de reconnexion de lecteurs déjà actifs, et ne met plus à jour les horodatages des sauvegardes.
* **Systèmes impactés :** Windows 10 (21H2 et ultérieurs), Windows 10 Enterprise LTSC 2016/2019, et Windows 11 (23H2 et ultérieurs).
* **Vulnérabilités :** Aucune CVE n'est associée à ce bug ; il s'agit d'une régression logicielle introduite par les correctifs de sécurité mensuels.

**Recommandations :**
* **Application immédiate :** Installer les mises à jour cumulatives optionnelles **KB5124006** (pour Windows 11 26H1) ou **KB5124010** (pour Windows 11 24H2/25H2) qui contiennent le correctif.
* **Solution alternative :** Pour les utilisateurs ne souhaitant pas installer de mises à jour optionnelles, le correctif sera intégré au prochain cycle de « Patch Tuesday » prévu pour le 13 octobre 2026.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-backup-feature-broken-by-september-updates/){:target="_blank"}
