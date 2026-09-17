---
title: 'Windows 11 KB5124008 update breaks domain trust for some users'
date: 2026-09-17
permalink: /posts/2026/09/17/windows-11-kb5124008-update-breaks-domain-trust-for-some-users/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes de confiance de domaine liés à la mise à jour KB5124008 de Windows 11

La mise à jour de sécurité KB5124008 pour Windows 11 provoque des ruptures de la relation de confiance entre les postes clients et les contrôleurs de domaine Active Directory. Cette défaillance empêche les utilisateurs de se connecter avec leurs identifiants de domaine, le système rejetant les authentifications malgré des informations valides.

**Points clés :**
* **Impact :** Les appareils perdent leur canal sécurisé avec Active Directory après redémarrage.
* **Cause suspectée :** Le dysfonctionnement est lié à la fonctionnalité « Machine Identity Isolation » (isolation de l'identité de la machine), activée en mode "enforcement" par la mise à jour, ce qui perturbe la gestion des secrets LSA via Credential Guard.
* **Vulnérabilité :** Il ne s'agit pas d'une faille CVE classique, mais d'une régression logicielle affectant l'intégrité de l'authentification Kerberos/NTLM au sein des environnements d'entreprise.

**Recommandations :**
* **Prudence :** Microsoft enquête officiellement ; aucune solution corrective définitive n'est publiée.
* **Contournement temporaire :** Certains administrateurs ont réussi à restaurer l'accès en réglant la valeur de registre `MachineIdentityIsolation` (située dans `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa`) sur `0`, puis en réparant le canal sécurisé via la commande PowerShell : 
  `Test-ComputerSecureChannel -Repair -Credential (Get-Credential)`.
* **Avertissement :** La modification ou la désactivation de « Machine Identity Isolation » après avoir été en mode "enforcement" peut entraîner des ruptures d'authentification supplémentaires nécessitant de retirer et de rejoindre le domaine. Procédez avec précaution et testez sur un échantillon restreint avant tout déploiement.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5124008-update-breaks-domain-trust-for-some-users/){:target="_blank"}
