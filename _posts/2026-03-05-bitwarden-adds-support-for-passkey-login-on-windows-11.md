---
title: 'Bitwarden adds support for passkey login on Windows 11'
date: 2026-03-05
permalink: /posts/2026/03/05/bitwarden-adds-support-for-passkey-login-on-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
## Authentification renforcée sur Windows 11 avec Bitwarden

Bitwarden propose désormais la connexion aux appareils sous Windows 11 via des clés d'accès (passkeys) stockées dans son coffre-fort. Cette fonctionnalité, disponible pour tous les utilisateurs, y compris ceux du forfait gratuit, permet une authentification résistante au phishing. L'accès est accordé en sélectionnant l'option de clé de sécurité et en scannant un code QR avec un appareil mobile pour confirmer l'utilisation de la clé d'accès enregistrée dans le coffre-fort chiffré de Bitwarden.

Pour utiliser cette nouvelle fonctionnalité, trois conditions sont nécessaires :
*   Disposer d'appareils joints à Microsoft Entra ID.
*   L'authentification par clé de sécurité FIDO2 doit être activée.
*   Une clé d'accès Entra ID doit être enregistrée dans le coffre-fort Bitwarden de l'utilisateur.

Bitwarden agit comme fournisseur de clés d'accès dans le processus d'authentification Windows. Les clés sont stockées dans le coffre-fort synchronisé de l'utilisateur, et non liées à un seul appareil, facilitant ainsi la récupération en cas de perte de téléphone. Cette méthode renforce significativement la sécurité en remplaçant les mots de passe par des défis cryptographiques signés, réduisant ainsi le risque d'exposition des identifiants au phishing. Microsoft prévoit de déployer cette fonctionnalité sur Windows 11 ce mois-ci, dépendant de la configuration d'Entra ID. Cette évolution s'appuie sur l'API de fournisseur de clés d'accès introduite par Microsoft en novembre 2025, permettant aux applications tierces comme Bitwarden de gérer les clés d'accès pour les sites web et les applications sur le système d'exploitation.

**Points clés :**
*   Prise en charge des clés d'accès pour la connexion Windows 11 via Bitwarden.
*   Authentification résistante au phishing et sans mot de passe.
*   Fonctionnalité disponible pour tous les plans Bitwarden.
*   Les clés d'accès sont stockées dans le coffre-fort chiffré et synchronisé de Bitwarden.
*   Permet la récupération sur d'autres appareils.

**Vulnérabilités :**
Aucune vulnérabilité spécifique n'est mentionnée dans l'article. L'ajout de cette fonctionnalité vise à renforcer la sécurité en remplaçant les méthodes d'authentification plus faibles.

**Recommandations :**
*   Assurez-vous que les prérequis (appareils joints à Entra ID, FIDO2 activé, clé d'accès Entra ID dans Bitwarden) sont remplis pour utiliser la fonctionnalité.
*   Utilisez Bitwarden pour stocker et gérer vos clés d'accès afin de bénéficier d'une authentification sécurisée sur Windows 11.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-adds-support-for-passkey-login-on-windows-11/){:target="_blank"}
