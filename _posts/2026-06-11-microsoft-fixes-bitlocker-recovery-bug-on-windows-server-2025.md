---
title: 'Microsoft fixes BitLocker recovery bug on Windows Server 2025'
date: 2026-06-11
permalink: /posts/2026/06/11/microsoft-fixes-bitlocker-recovery-bug-on-windows-server-2025/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution du bug de récupération BitLocker sur Windows Server 2025

Microsoft a déployé un correctif pour un problème affectant Windows Server 2025 et Windows 11, où l'installation de mises à jour système forçait les appareils à basculer en mode de récupération BitLocker. Ce comportement survient uniquement sur des systèmes présentant des configurations de stratégie de groupe spécifiques liées aux profils de validation PCR7 (Platform Configuration Register 7) dans un environnement UEFI.

**Points clés :**
* Le problème est lié à une incompatibilité lors de la mise à jour vers le gestionnaire de démarrage (Boot Manager) signé en 2023.
* L'incident ne concerne majoritairement que les systèmes en entreprise utilisant des politiques de groupe spécifiques et non les appareils personnels.
* La saisie de la clé de récupération n'est nécessaire qu'une seule fois si la configuration reste inchangée.
* Les mises à jour cumulatives de juin 2026 (**KB5094125** pour Windows Server 2025 et **KB5093998** pour Windows 11) corrigent définitivement ce comportement.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet incident, car il s'agit d'un bug de configuration logicielle lié à la gestion du démarrage sécurisé (Secure Boot) et non d'une faille de sécurité exploitable.

**Recommandations :**
* **Appliquer les mises à jour :** Installer les mises à jour cumulatives de juin 2026 pour résoudre le problème.
* **Gestion des stratégies :** Pour les administrateurs ne pouvant pas mettre à jour immédiatement, il est conseillé de retirer la stratégie de groupe "Configure TPM platform validation profile for native UEFI firmware configurations" et de s'assurer que les liaisons BitLocker utilisent le profil PCR7.
* **Known Issue Rollback (KIR) :** Utiliser cette fonctionnalité pour empêcher le basculement automatique vers le gestionnaire de démarrage 2023 si le déploiement immédiat des correctifs n'est pas possible.
* **Monitoring :** Surveiller l'identifiant d'événement (Event ID) 1032 dans les journaux système pour identifier les machines impactées par l'échec de mise à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bitlocker-recovery-bug-on-windows-server-2025/){:target="_blank"}
