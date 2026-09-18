---
title: 'Microsoft fixes broken copy and paste for Excel 2016 users'
date: 2026-09-18
permalink: /posts/2026/09/18/microsoft-fixes-broken-copy-and-paste-for-excel-2016-users/
tags:
- veille-cyber
- bleepingcomp
---
### Correction du dysfonctionnement du copier-coller dans Microsoft Excel

Une régression introduite par la mise à jour de sécurité **KB5002914** (septembre 2026) provoque une défaillance silencieuse des fonctions de copier-coller, de remplissage automatique et de glissement de formules dans plusieurs versions d'Excel (2016, 2019, 2021, 2024 et Online).

**Points clés :**
* Le bug empêche le transfert de données sans générer de message d'erreur ou d'alerte sonore.
* Microsoft a publié le correctif **KB5002665** spécifiquement pour les versions MSI d'Office 2016.
* Les éditions « Démarrer en un clic » (Click-to-Run) d'Office 2016, ainsi que les versions 2019, 2021 et 2024, ne sont pas officiellement couvertes par ce correctif, bien que des mises à jour récentes puissent avoir résolu le problème pour ces versions.

**Vulnérabilités :**
* Aucune CVE n'est associée à ce bug fonctionnel. Cependant, il est fortement déconseillé de désinstaller la mise à jour **KB5002914**, car cette dernière contient des correctifs critiques pour des failles d'exécution de code à distance (RCE) et de divulgation d'informations.

**Recommandations :**
* **Solution temporaire :** Utiliser la fonction « Collage spécial » via le menu « Accueil » ou le raccourci `Ctrl+Alt+V` pour contourner le bug.
* **Mise à jour :** Installer la mise à jour **KB5002665** pour les utilisateurs d'Office 2016 (MSI).
* **Sécurité :** Éviter de désinstaller la mise à jour KB5002914 pour ne pas exposer le système à des risques de sécurité majeurs. Si la désinstallation est indispensable pour des impératifs opérationnels, elle doit être effectuée via l'invite de commande avec des privilèges administrateur (voir les commandes spécifiques fournies par Microsoft pour chaque version).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-broken-copy-and-paste-for-excel-2016-users/){:target="_blank"}
