---
title: 'Certighost and the Privilege Hiding in Your Certificate Authority'
date: 2026-08-17
permalink: /posts/2026/08/17/certighost-and-the-privilege-hiding-in-your-certificate-authority/
tags:
- veille-cyber
- bleepingcomp
---
### Certighost : Quand la confiance aveugle envers l'autorité de certification compromet le domaine

La vulnérabilité **Certighost (CVE-2026-54121)**, notée 8.8 sur l'échelle CVSS, permet à un utilisateur standard du domaine d'obtenir un certificat valide pour un contrôleur de domaine (DC), usurpant ainsi son identité et prenant potentiellement le contrôle total de l'Active Directory.

**Points clés :**
*   **Mécanisme de l'attaque :** La faille repose sur la fonctionnalité "chase" d'Active Directory Certificate Services (AD CS). L'autorité de certification (CA) accepte des informations de routage fournies par l'utilisateur (paramètre `cdc`) sans vérifier si la destination est un contrôleur de domaine légitime.
*   **Escalade de privilèges :** L'attaquant force la CA à se connecter à un point de terminaison malveillant, récupère un certificat signé pour un compte de contrôleur de domaine, puis utilise PKINIT pour obtenir des tickets Kerberos, permettant des opérations DCSync et le vol de secrets (ex: `krbtgt`).
*   **Facteur aggravant :** L'attaque exploite le paramètre par défaut `MachineAccountQuota`, qui autorise tout utilisateur authentifié à créer des comptes de machine dans l'Active Directory.

**Vulnérabilité :**
*   **CVE-2026-54121 :** Défaut de validation de destination lors de l'enrôlement de certificats dans AD CS.

**Recommandations :**
*   **Correctif immédiat :** Appliquer la mise à jour de sécurité Microsoft du 14 juillet 2026 sur toutes les autorités de certification.
*   **Configuration système :** Réduire le `MachineAccountQuota` à zéro pour empêcher la création arbitraire de comptes de machine par des utilisateurs non privilégiés.
*   **Durcissement réseau :** Restreindre les flux sortants (SMB et LDAP) des serveurs de CA pour qu'ils ne puissent communiquer qu'avec des contrôleurs de domaine approuvés.
*   **Audit et Monitoring :** Surveiller étroitement la création de comptes de machine, les enrôlements de certificats suspects et toute tentative de DCSync provenant de sources non autorisées.
*   **Gouvernance :** Réviser les permissions des modèles de certificats et appliquer le principe du moindre privilège, considérant l'autorité de certification comme une infrastructure critique et non comme un simple utilitaire.

---
[Source](https://www.bleepingcomputer.com/news/security/certighost-and-the-privilege-hiding-in-your-certificate-authority/){:target="_blank"}
