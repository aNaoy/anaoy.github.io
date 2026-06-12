---
title: 'Microsoft fixes Windows update failures linked to WUSA installer'
date: 2026-06-12
permalink: /posts/2026/06/12/microsoft-fixes-windows-update-failures-linked-to-wusa-installer/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des échecs de mise à jour Windows via l'outil WUSA

Microsoft a corrigé un bug technique affectant l'outil *Windows Update Standalone Installer* (WUSA), qui empêchait l'installation correcte des mises à jour lorsque celles-ci étaient déployées depuis un partage réseau contenant plusieurs fichiers `.msu`.

**Points clés :**
* **Systèmes impactés :** Windows 11 (versions 24H2/25H2) et Windows Server 2025.
* **Origine du problème :** Le bug survenait lors de l'exécution de fichiers `.msu` à partir d'un dossier réseau, provoquant l'erreur `ERROR_BAD_PATHNAME`.
* **Chronologie :** Le problème a été identifié en mai 2025 (KB5058499) et a fait l'objet d'un correctif définitif lors du cycle de maintenance (Patch Tuesday) de juin 2026.
* **Vulnérabilités :** Aucune CVE n'est associée à cet incident, il s'agit d'un dysfonctionnement opérationnel et non d'une faille de sécurité exploitable.

**Recommandations :**
* **Application des correctifs :** Installez les mises à jour cumulatives de juin 2026 : **KB5079391** (Windows 11) ou **KB5094125** (Windows Server 2025).
* **Contournement temporaire :** Si vous utilisez une version antérieure, téléchargez et installez les fichiers `.msu` localement sur la machine plutôt que depuis un partage réseau.
* **Vérification :** Après l'installation via WUSA, patientez au moins 15 minutes avant de consulter l'historique des mises à jour dans les Paramètres pour garantir que le statut de l'installation soit correctement mis à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-update-failures-linked-to-wusa-installer/){:target="_blank"}
