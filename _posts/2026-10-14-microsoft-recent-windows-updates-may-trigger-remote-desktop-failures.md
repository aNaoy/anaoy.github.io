---
title: 'Microsoft: Recent Windows updates may trigger Remote Desktop failures'
date: 2026-10-14
permalink: /posts/2026/10/14/microsoft-recent-windows-updates-may-trigger-remote-desktop-failures/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement du Bureau à distance lié à la protection administrateur sous Windows 11

Les récentes mises à jour de Windows 11 (versions 24H2, 25H2, 26H1 et 26H2) entraînent des échecs de connexion au Bureau à distance sur les systèmes où la fonctionnalité « Protection administrateur » (Administrator Protection) est activée.

**Points clés :**
*   **Cause du problème :** La fonctionnalité de protection administrateur, activée par défaut dans les bases de référence de sécurité (security baselines) depuis octobre 2026, entre en conflit avec le service de Bureau à distance.
*   **Symptôme :** Les tentatives de connexion échouent avec l'erreur `0xC000000D` et le message « The token that was passed to the function is invalid ».
*   **Impact :** Ce problème concerne principalement les appareils gérés en entreprise agissant comme hôtes pour le Bureau à distance.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, il s'agit d'une régression logicielle induite par les mises à jour (notamment KB5124010).

**Recommandations :**
*   **Contournement temporaire :** Microsoft préconise aux administrateurs informatiques de désactiver la « Protection administrateur » via les outils de gestion de stratégie (Microsoft Intune ou Stratégie de groupe).
*   **Action spécifique :** Réinitialiser la stratégie « User Account Control: Admin Approval Mode » (Type de contrôle de compte d'utilisateur du mode d'approbation administrateur).
*   **Veille :** Surveiller les prochains bulletins de sécurité de Microsoft pour une correction définitive du problème.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-recent-windows-updates-may-trigger-remote-desktop-failures/){:target="_blank"}
