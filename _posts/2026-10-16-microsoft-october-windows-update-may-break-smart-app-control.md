---
title: 'Microsoft: October Windows update may break Smart App Control'
date: 2026-10-16
permalink: /posts/2026/10/16/microsoft-october-windows-update-may-break-smart-app-control/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement du Smart App Control après la mise à jour Windows d'octobre

La mise à jour de sécurité **KB5127648** déployée par Microsoft pour Windows 11 (versions 24H2 et ultérieures) empêche certains utilisateurs d'activer la fonctionnalité « Smart App Control ». Sur les systèmes concernés, l'option apparaît grisée dans l'application Sécurité Windows. Les appareils où la fonctionnalité était déjà active avant l'installation de la mise à jour ne sont pas impactés et demeurent sécurisés.

**Points clés :**
*   **Fonctionnalité impactée :** Smart App Control, qui bloque les applications potentiellement malveillantes.
*   **Périmètre :** Windows 11 version 24H2 et versions supérieures ayant installé la mise à jour KB5127648.
*   **Vulnérabilité :** Il ne s'agit pas d'une faille de sécurité exploitable, mais d'un bug système de configuration empêchant l'activation d'un outil de protection. Aucune CVE n'est associée à cet incident.

**Recommandations :**
En attendant un correctif officiel, Microsoft propose deux méthodes de contournement pour les administrateurs :
1.  **Modification du Registre :** Exécuter les commandes suivantes via une invite de commande (Admin) puis redémarrer :
    *   `reg add "HKLM\SYSTEM\CurrentControlSet\Policies\Microsoft\FeatureManagement\Overrides" /v 2883193997 /t REG_DWORD /d 1 /f`
    *   `reg add "HKLM\SYSTEM\CurrentControlSet\Policies\Microsoft\FeatureManagement\Overrides" /v 2850574478 /t REG_DWORD /d 1 /f`
2.  **Stratégie de groupe (GPO) :** Installer les fichiers de prévisualisation de fonctionnalités (KB5074105) fournis par Microsoft, activer les deux paramètres correspondants sous *Configuration ordinateur > Modèles d'administration*, puis redémarrer les machines.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/kb5127648-windows-security-update-may-break-smart-app-control/){:target="_blank"}
