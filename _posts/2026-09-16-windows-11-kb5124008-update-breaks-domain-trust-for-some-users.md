---
title: 'Windows 11 KB5124008 update breaks domain trust for some users'
date: 2026-09-16
permalink: /posts/2026/09/16/windows-11-kb5124008-update-breaks-domain-trust-for-some-users/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement de la relation d'approbation de domaine après la mise à jour KB5124008

La mise à jour de sécurité Windows 11 KB5124008 provoque une rupture de la relation d'approbation entre les postes clients et Active Directory, empêchant les utilisateurs de se connecter avec leurs identifiants de domaine. Le problème survient au redémarrage suivant l'installation de la mise à jour, entraînant des échecs d'authentification Kerberos et des replis vers NTLM/Netlogon.

**Points clés :**
* **Cause probable :** Le dysfonctionnement est lié à la fonctionnalité de sécurité « Machine Identity Isolation », qui passe automatiquement en mode « enforcement » (valeur 2) après l'installation de la mise à jour.
* **Impact :** Les secrets des comptes machine sont déplacés vers Credential Guard, rompant le canal sécurisé avec le contrôleur de domaine.
* **Absence de correctif officiel :** Microsoft enquête actuellement sur le problème et n'a pas encore publié de solution officielle.

**Vulnérabilités :**
Aucune CVE n'est associée à cet incident. Il s'agit d'une régression logicielle introduite par une mise à jour de sécurité.

**Recommandations :**
* **Prudence :** Évitez de désactiver arbitrairement la fonctionnalité `MachineIdentityIsolation` via le registre (clé `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa`), car cela peut entraîner des ruptures d'authentification supplémentaires sur des systèmes sains.
* **Procédure de contournement (si nécessaire) :** Certains administrateurs ont réussi à restaurer l'accès en désactivant la fonctionnalité (passer à '0'), redémarrant, puis en réparant le canal sécurisé via PowerShell :
  `Test-ComputerSecureChannel -Repair -Credential(Get-Credential)`
* **Veille :** Surveillez les communications officielles de Microsoft pour obtenir une solution stabilisée.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5124008-update-breaks-domain-trust-for-some-users/){:target="_blank"}
