---
title: 'Bitwarden adds support for passkey login on Windows 11'
date: 2026-03-05
permalink: /posts/2026/03/05/bitwarden-adds-support-for-passkey-login-on-windows-11/
tags:
- veille-cyber
- bleepingcomp
---
### Authentification sans mot de passe sur Windows 11 via Bitwarden

Bitwarden intègre désormais la prise en charge des passkeys pour l'authentification native sur Windows 11. Cette fonctionnalité, disponible pour tous les utilisateurs, permet de remplacer les mots de passe traditionnels par des identifiants cryptographiques stockés dans le coffre-fort Bitwarden, réduisant ainsi considérablement l'exposition aux attaques par phishing.

**Points clés :**
* **Interopérabilité :** Les passkeys sont synchronisés via le coffre-fort Bitwarden, permettant une récupération multi-appareils, contrairement à un stockage lié à une machine unique.
* **Fonctionnement :** Lors de la connexion, l'utilisateur sélectionne l'option de clé de sécurité et valide l'accès en scannant un QR code avec son appareil mobile.
* **Couverture :** Cette mise à jour étend l'API de gestion des passkeys de Windows 11, introduite fin 2025, au niveau de l'authentification système.

**Vulnérabilités :**
* Aucune vulnérabilité spécifique (CVE) n'est associée à cette annonce. Le déploiement vise précisément à mitiger les risques de vol de justificatifs (phishing) liés à l'utilisation des mots de passe classiques.

**Recommandations :**
* **Prérequis techniques :** Pour bénéficier de cette fonctionnalité, les appareils doivent être joints à Microsoft Entra ID et l'option de connexion par clé de sécurité FIDO2 doit être activée au sein de la configuration Entra ID de l'organisation.
* **Gestion des accès :** Veiller à ce que les passkeys soient correctement enregistrés dans le coffre-fort Bitwarden avant d'activer la connexion sans mot de passe sur les postes de travail.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-adds-support-for-passkey-login-on-windows-11/){:target="_blank"}
