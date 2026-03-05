---
title: 'Bitwarden adds support for passkey login on Windows 11'
date: 2026-03-05
permalink: /posts/2026/03/05/bitwarden-adds-support-for-passkey-login-on-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
**Bitwarden Intègre les Passkeys pour l'Accès à Windows 11**

Bitwarden, le gestionnaire de mots de passe et de secrets open-source, propose désormais une fonctionnalité permettant de se connecter aux appareils Windows 11 en utilisant des passkeys stockées dans son coffre-fort. Cette intégration vise à renforcer la sécurité en offrant une authentification résistante au phishing.

La nouvelle fonctionnalité est disponible pour tous les utilisateurs, y compris ceux du forfait gratuit. Pour l'utiliser, les utilisateurs doivent répondre à trois conditions : disposer d'appareils joints à Entra ID, activer la connexion via une clé de sécurité FIDO2, et posséder une passkey Entra ID enregistrée dans leur coffre-fort Bitwarden.

Le processus implique la sélection de l'option de clé de sécurité lors de la connexion à Windows, suivi de la numérisation d'un code QR avec un appareil mobile pour confirmer l'accès à la passkey. Bitwarden agit comme fournisseur de passkey dans le flux d'authentification Windows, stockant la clé dans le coffre-fort synchronisé de l'utilisateur plutôt que de la lier à un seul appareil, ce qui facilite la récupération en cas de perte de téléphone.

En remplaçant la saisie de mot de passe par des défis cryptographiques signés avec des clés privées, cette méthode réduit considérablement le risque d'exposition des identifiants. Microsoft déploie actuellement cette fonctionnalité sur Windows 11, en fonction de la configuration d'Entra ID. Cette avancée étend la prise en charge des passkeys, introduite par Microsoft pour les applications tierces en novembre 2025, à une couche d'authentification plus fondamentale, celle du système d'exploitation lui-même.

**Points Clés :**

*   Bitwarden permet la connexion à Windows 11 avec des passkeys.
*   Cette méthode offre une authentification résistante au phishing.
*   La fonctionnalité est accessible à tous les plans de Bitwarden.
*   Les passkeys sont stockées de manière sécurisée dans le coffre-fort Bitwarden et synchronisées sur tous les appareils.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (avec CVE) n'est mentionnée dans cet article. La fonctionnalité vise à prévenir les risques liés aux vulnérabilités de phishing associées aux mots de passe traditionnels.

**Recommandations :**

*   Utiliser des appareils joints à Entra ID.
*   Activer la connexion via une clé de sécurité FIDO2.
*   Enregistrer une passkey Entra ID dans son coffre-fort Bitwarden.
*   S'assurer que la configuration d'Entra ID sur Windows 11 est prête pour le déploiement de la fonctionnalité.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-adds-support-for-passkey-login-on-windows-11/){:target="_blank"}
