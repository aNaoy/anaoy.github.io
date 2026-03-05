---
title: 'Bitwarden adds support for passkey login on Windows 11'
date: 2026-03-05
permalink: /posts/2026/03/05/bitwarden-adds-support-for-passkey-login-on-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
**Bitwarden Intègre la Connexion par Passkey sur Windows 11**

Bitwarden introduit la prise en charge des passkeys pour la connexion aux appareils sous Windows 11. Cette fonctionnalité permet une authentification résistante au phishing, utilisant des clés cryptographiques plutôt que des mots de passe. Les passkeys stockées dans le coffre-fort Bitwarden sécurisé peuvent désormais être utilisées pour accéder au système d'exploitation, offrant une couche de sécurité supplémentaire.

Cette nouvelle capacité est accessible à tous les utilisateurs, y compris ceux du plan gratuit. Pour l'utiliser, il est nécessaire d'avoir des appareils joints à Entra ID, que la connexion par clé de sécurité FIDO2 soit activée, et de posséder une passkey Entra ID enregistrée dans son coffre-fort Bitwarden.

Bitwarden agit comme fournisseur de passkey dans le processus d'authentification Windows, stockant les identifiants dans le coffre-fort synchronisé de l'utilisateur, ce qui facilite la récupération depuis d'autres appareils en cas de perte de téléphone. L'élimination de la saisie de mots de passe réduit considérablement le risque d'exposition aux attaques de phishing.

Cette évolution s'appuie sur l'API de fournisseur de passkey introduite par Microsoft pour Windows 11 en novembre 2025, permettant aux applications tierces de gérer les passkeys. L'intégration actuelle va plus loin en l'appliquant à la couche d'authentification du système d'exploitation lui-même.

**Points Clés :**

*   **Nouvelle Fonctionnalité :** Connexion à Windows 11 via des passkeys stockées dans Bitwarden.
*   **Sécurité Améliorée :** Authentification résistante au phishing grâce à des identifiants cryptographiques.
*   **Accessibilité :** Disponible pour tous les plans, y compris gratuit.
*   **Flexibilité :** Les passkeys sont liées au coffre-fort synchronisé, permettant une récupération facile.

**Vulnérabilités (Non Spécifiées dans l'article) :**

L'article ne détaille pas de vulnérabilités spécifiques liées à cette nouvelle fonctionnalité.

**Recommandations :**

*   Assurez-vous que vos appareils Windows 11 sont joints à Entra ID.
*   Vérifiez que la connexion par clé de sécurité FIDO2 est activée.
*   Enregistrez vos passkeys Entra ID dans votre coffre-fort Bitwarden.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-adds-support-for-passkey-login-on-windows-11/){:target="_blank"}
