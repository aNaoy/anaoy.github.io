---
title: 'Bitwarden adds support for passkey login on Windows 11'
date: 2026-03-05
permalink: /posts/2026/03/05/bitwarden-adds-support-for-passkey-login-on-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
### Authentification Sans Mot de Passe pour Windows 11 avec Bitwarden

Bitwarden intègre désormais la prise en charge des passkeys pour la connexion aux appareils sous Windows 11, offrant une méthode d'authentification résistante au phishing. Cette fonctionnalité, disponible pour tous les utilisateurs, y compris ceux du plan gratuit, permet de se connecter à Windows en utilisant une passkey stockée dans le coffre-fort chiffré de Bitwarden. L'utilisateur sélectionne l'option de clé de sécurité et scanne un code QR avec son appareil mobile pour confirmer l'accès.

Bitwarden, un gestionnaire de mots de passe et de secrets open-source, peut stocker divers types d'informations sensibles, y compris les mots de passe, les passkeys, les clés API, les détails de cartes de crédit, les données d'identité et les notes privées.

Pour utiliser cette nouvelle fonctionnalité, trois conditions doivent être remplies :
1.  Disposer d'appareils joints à Microsoft Entra ID.
2.  L'option de connexion via une clé de sécurité FIDO2 doit être activée.
3.  Une passkey Entra ID enregistrée doit être stockée dans le coffre-fort Bitwarden de l'utilisateur.

Bitwarden agit comme le fournisseur de passkey dans le processus d'authentification de Windows, stockant les identifiants de manière synchronisée dans le coffre-fort de l'utilisateur, plutôt que de les lier à un appareil unique. Cela permet également la récupération via d'autres appareils en cas de perte du téléphone. L'élimination de la saisie de mot de passe et l'utilisation d'authentification cryptographique réduisent considérablement le risque d'exposition des identifiants au phishing.

Microsoft déploie cette fonctionnalité de connexion par passkey sur Windows ce mois-ci, dépendant de la configuration de Microsoft Entra ID. Cette avancée s'appuie sur l'introduction par Microsoft en novembre 2025 d'une API de fournisseur de passkeys pour Windows 11, permettant à des applications tierces de gérer nativement les passkeys pour les sites web et les applications. L'intégration de Bitwarden étend cette capacité à la couche d'authentification fondamentale du système d'exploitation lui-même.

**Points Clés :**

*   Bitwarden permet désormais la connexion à Windows 11 via des passkeys.
*   Cette méthode est résistante au phishing.
*   La fonctionnalité est accessible à tous les plans, y compris le gratuit.
*   La passkey est stockée dans le coffre-fort Bitwarden synchronisé, permettant la récupération sur d'autres appareils.
*   Cela étend la prise en charge des passkeys du niveau applicatif au niveau du système d'exploitation.

**Vulnérabilités :**
Aucune vulnérabilité spécifique (avec CVE) n'est mentionnée dans l'article.

**Recommandations :**
*   Utiliser des appareils joints à Microsoft Entra ID.
*   Activer la connexion via une clé de sécurité FIDO2.
*   Enregistrer et stocker une passkey Entra ID dans son coffre-fort Bitwarden.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-adds-support-for-passkey-login-on-windows-11/){:target="_blank"}
