---
title: 'New phishing kits target Microsoft 365 accounts, evade MFA'
date: 2026-07-14
permalink: /posts/2026/07/14/new-phishing-kits-target-microsoft-365-accounts-evade-mfa/
tags:
- veille-cyber
- bleepingcomp
---
### Menaces persistentes contre Microsoft 365 : Jalisco et OmegaLord

De nouveaux kits de phishing, nommés **Jalisco** et **OmegaLord**, ciblent les comptes Microsoft 365 en contournant activement les protections par authentification multifacteur (MFA).

**Points clés :**
* **Jalisco (Phishing par code d'appareil) :** Exploite le flux d'autorisation OAuth 2.0. Il génère des codes en temps réel pour tromper les victimes, leur faisant autoriser un appareil contrôlé par l'attaquant. Une fois lié, l'attaquant accède au compte sans mot de passe.
* **OmegaLord (Phishing conventionnel) :** Utilise une fausse interface de lecteur PDF pour récolter identifiants et numéros de téléphone. Cette collecte vise spécifiquement à faciliter l'interception ou le détournement des codes MFA.
* **Impact :** Une fois le compte compromis, les attaquants exfiltrent des données sensibles (SharePoint, PII, documents financiers) en moins de six minutes, avant de lancer des demandes d'extorsion.
* **Vulnérabilités :** L'article ne mentionne pas de CVE spécifique, car il s'agit d'un détournement de fonctionnalités légitimes (OAuth 2.0 Device Authorization Grant) et non d'une faille logicielle.

**Recommandations :**
* **Réduction de la surface d'attaque :** Limiter le nombre de dispositifs enregistrés par utilisateur dans Entra ID (passer de la valeur par défaut de 50 à 1 ou 2).
* **Contrôles d'accès :** Bloquer l'authentification par code d'appareil via les stratégies d'accès conditionnel (Microsoft Entra Conditional Access).
* **Gestion OAuth :** Restreindre l'octroi d'autorisation d'appareil dans les plateformes de gestion d'identité (type Okta).
* **Audit :** Procéder à un inventaire régulier et supprimer toutes les inscriptions d'applications inutilisées ou suspectes.

---
[Source](https://www.bleepingcomputer.com/news/security/new-phishing-kits-target-microsoft-365-accounts-evade-mfa/){:target="_blank"}
