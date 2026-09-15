---
title: 'Microsoft releases emergency Windows updates to fix RDS failures'
date: 2026-09-15
permalink: /posts/2026/09/15/microsoft-releases-emergency-windows-updates-to-fix-rds-failures/
tags:
- veille-cyber
- bleepingcomp
---
### Correctifs d'urgence pour les instabilités des services Windows

Microsoft a déployé des mises à jour correctives « hors bande » pour résoudre des dysfonctionnements critiques introduits par les mises à jour de sécurité de septembre 2026. Ces failles affectaient principalement les services Bureau à distance (RDS), la virtualisation Hyper-V et certains périphériques audio USB.

**Points clés :**
* **Instabilité RDS :** Les mises à jour précédentes provoquaient des échecs de connexion, des blocages du serveur et des dysfonctionnements dans des outils essentiels tels que l'Explorateur de fichiers et la console de gestion (MMC).
* **Virtualisation :** Correction d'un problème empêchant l'accès aux dossiers partagés entre un hôte Windows et des machines virtuelles Linux (via Plan9).
* **Audio USB :** Résolution partielle des problèmes sur les périphériques USB Audio Class 1.0 (notamment en mode multicanal), bien que certains bugs de lecture audio persistent.

**Vulnérabilités et correctifs associés :**
* Aucun numéro de CVE spécifique n'a été associé à ces bugs fonctionnels, car il s'agit de régressions logicielles (bugs de mise à jour) plutôt que de vulnérabilités exploitables.
* **KB correctifs :** 
    * Windows 10 (21H2/22H2) : KB5129236
    * Windows 11 (24H2/25H2) : KB5129195
    * Windows 11 (26H1) : KB5129194
    * Windows Server 2019 : KB5129238
    * Windows Server 2022 : KB5129237
    * Windows Server 2025 : KB5129235

**Recommandations :**
* **Déploiement immédiat :** Installer les mises à jour mentionnées ci-dessus via Windows Update ou le catalogue Microsoft Update pour rétablir la stabilité du système.
* **Éviter la désinstallation :** Ne pas désinstaller manuellement les mises à jour de sécurité de septembre, car cela exposerait les systèmes à des failles de sécurité réelles.
* **Surveillance :** Pour les utilisateurs de périphériques USB Audio Class 1.0, rester attentif aux futures communications de Microsoft, car une partie des problèmes audio reste en attente d'un correctif définitif.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-emergency-windows-updates-to-fix-rds-failures/){:target="_blank"}
