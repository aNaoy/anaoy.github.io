---
title: 'Microsoft shares workaround for Windows domain login issues'
date: 2026-09-17
permalink: /posts/2026/09/17/microsoft-shares-workaround-for-windows-domain-login-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes d'authentification sur les domaines Windows suite aux mises à jour de septembre 2026

Les mises à jour de sécurité de septembre 2026 (KB5124008 et KB5124012) provoquent des erreurs de confiance de domaine sur Windows 11 (versions 24H2, 25H2 et 26H1). Le dysfonctionnement empêche l'ouverture de session malgré des identifiants valides.

**Points clés :**
* **Cause :** L'activation du mécanisme « Machine Identity Isolation » en mode application.
* **Compatibilité :** Cette fonctionnalité n'est officiellement supportée que dans les environnements utilisant des contrôleurs de domaine sous Windows Server 2025 (DFL et supérieur).
* **Impact :** Les appareils configurés avec cette option dans des environnements non compatibles perdent leur relation de confiance sécurisée avec le domaine.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet incident. Il s'agit d'un problème de compatibilité logicielle induit par une mise à jour système.

**Recommandations :**
* **Désactivation :** Les administrateurs doivent désactiver la fonctionnalité « Machine Identity Isolation » via la méthode utilisée pour l'implémenter (Intune, GPO ou registre).
* **Procédure manuelle (Registre) :**
    1. Accéder aux clés : `HKLM\SYSTEM\CurrentControlSet\Control\Lsa\MachineIdentityIsolation` et `HKLM\SOFTWARE\Policies\Microsoft\Windows\DeviceGuard\MachineIdentityIsolation`.
    2. Modifier la valeur de `MachineIdentityIsolation` à `0`.
    3. Redémarrer la machine.
    4. Réinitialiser le canal sécurisé via la commande PowerShell : `Test-ComputerSecureChannel -Repair -Credential (Get-Credential)`.
* **Note importante :** Si la fonctionnalité a été activée puis désactivée sans précaution, il peut être nécessaire de sortir la machine du domaine, puis de la réintégrer.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-workaround-for-windows-domain-login-authentication-issues/){:target="_blank"}
