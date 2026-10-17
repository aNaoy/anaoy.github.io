---
title: 'Hackers breach Microsoft 365 tenants via ConnectWise supply-chain attack'
date: 2026-10-17
permalink: /posts/2026/10/17/hackers-breach-microsoft-365-tenants-via-connectwise-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement visant Microsoft 365 via ConnectWise

ConnectWise a suspendu son service "Cloud Backup" (anciennement SkyKick) suite à une intrusion permettant à des attaquants d'exploiter des identités d'application pour accéder aux tenants Microsoft 365 des clients. L'attaque, détectée dès le 15 octobre, consiste à utiliser des identifiants d'application légitimes pour contourner l'authentification multifacteur (MFA), car les accès s'effectuent via des jetons d'application déjà autorisés.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation abusive des permissions (notamment *Directory.ReadWrite.All*) accordées aux applications ConnectWise dans les tenants Microsoft 365.
*   **Méthode :** Script automatisé utilisant l'adresse IP `144.172.64.128` pour s'authentifier directement via les secrets d'application.
*   **Impact :** Accès non autorisé aux e-mails, fichiers OneDrive/SharePoint et conversations Teams. Dans certains cas, les attaquants ont élevé leurs privilèges (rôle administrateur global) pour établir une persistance en ajoutant leurs propres identifiants.
*   **Vulnérabilités :** Aucune CVE n'est associée, il s'agit d'un abus de privilèges légitimes (Supply-Chain Attack) où l'application possédait des droits trop larges.

**Recommandations :**
*   **Audit immédiat :** Vérifier les journaux d'Entra ID pour détecter des connexions suspectes ou des changements de rôles/identifiants initiés par les applications ConnectWise.
*   **Suppression des accès :** Désactiver les applications ConnectWise concernées et supprimer manuellement tout identifiant, secret ou certificat ajouté de manière non autorisée depuis le 13 octobre.
*   **Revocation :** Garder à l'esprit que la désactivation d'une application ne révoque pas nécessairement les jetons d'accès déjà actifs ; une vigilance accrue sur les activités Graph API est nécessaire.
*   **Surveillance :** Inspecter spécifiquement les IDs d'application listés par ConnectWise (ex: `506e08f9-6e9a-4da4-942b-a099a03644ae` pour Cloud Backup).

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breach-microsoft-365-tenants-via-connectwise-supply-chain-attack/){:target="_blank"}
