---
title: 'Microsoft: April updates trigger BitLocker key prompts on some servers'
date: 2026-04-15
permalink: /posts/2026/04/15/microsoft-april-updates-trigger-bitlocker-key-prompts-on-some-servers/
tags:
- veille-cyber
- bleepingcomp
---
### Incidents de récupération BitLocker après la mise à jour KB5082063

L'installation de la mise à jour de sécurité d'avril 2026 (KB5082063) sur certains serveurs Windows Server 2025 provoque un déclenchement inattendu du mode de récupération BitLocker lors du redémarrage. Ce phénomène n'est pas une vulnérabilité de sécurité, mais un problème de configuration spécifique lié à la gestion des clés de chiffrement au démarrage.

**Points clés :**
*   Le problème se produit lors du premier redémarrage après la mise à jour ; les redémarrages ultérieurs sont épargnés si la configuration reste inchangée.
*   L'impact est limité aux environnements d'entreprise possédant des configurations de stratégie de groupe (GPO) spécifiques.
*   Le souci survient lorsque le système bascule vers le nouveau gestionnaire de démarrage signé en 2023.

**Conditions de déclenchement :**
Pour que le problème survienne, les cinq conditions suivantes doivent être réunies :
1. BitLocker activé sur le disque système.
2. Configuration de la GPO "Configure TPM platform validation profile for native UEFI" incluant le PCR7.
3. État Secure Boot PCR7 Binding rapporté comme "Not Possible" dans `msinfo32.exe`.
4. Présence du certificat Windows UEFI CA 2023 dans la base de données de signature (DB) du Secure Boot.
5. Le système utilise actuellement une version du gestionnaire de démarrage antérieure à celle signée en 2023.

**Recommandations :**
*   **Avant déploiement :** Supprimer la configuration de la stratégie de groupe liée au profil PCR7 avant d'installer la mise à jour KB5082063.
*   **Alternative :** Si la suppression de la GPO est impossible, appliquer un "Known Issue Rollback" (KIR) pour empêcher le basculement automatique vers le gestionnaire de démarrage 2023 et éviter ainsi la récupération BitLocker.
*   **Procédure de récupération :** En cas de blocage sur l'écran de récupération, la saisie manuelle de la clé de récupération BitLocker est nécessaire pour restaurer l'accès au système.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-some-windows-servers-ask-for-bitlocker-key-after-april-updates/){:target="_blank"}
