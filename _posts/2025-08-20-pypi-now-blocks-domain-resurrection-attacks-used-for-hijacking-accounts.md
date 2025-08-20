---
title: 'PyPI now blocks domain resurrection attacks used for hijacking accounts'
date: 2025-08-20
permalink: /posts/2025/08/20/pypi-now-blocks-domain-resurrection-attacks-used-for-hijacking-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### PyPI Renforce la Sécurité contre le Détournement de Comptes via Domaines Expirés

Le Python Package Index (PyPI) a implémenté de nouvelles mesures pour contrer les attaques par résurrection de domaines, une méthode permettant le détournement de comptes par le biais de réinitialisations de mot de passe. Ces attaques exploitent l'expiration de noms de domaine liés aux adresses e-mail des mainteneurs de projets, permettant aux attaquants de reprendre le contrôle d'un compte en enregistrant le domaine expiré et en sollicitant une réinitialisation de mot de passe. Le risque principal est celui d'une attaque sur la chaîne d'approvisionnement logicielle, où des projets piratés publieraient des versions malveillantes de paquets populaires.

Un exemple notable fut le détournement du paquet 'ctx' en mai 2022, qui incluait du code destiné à voler des informations d'identification AWS.

Les nouvelles protections de PyPI consistent à vérifier le statut d'expiration des domaines associés aux adresses e-mail vérifiées. Les adresses dont les domaines sont expirés ou en phase d'expiration sont marquées comme non vérifiées, les rendant inutilisables pour les réinitialisations de mot de passe ou la récupération de compte. PyPI utilise l'API Status de Domainr pour évaluer le cycle de vie des domaines. Ces mesures, développées depuis avril 2025 et déployées en juin 2025, ont déjà conduit à la non-vérification de plus de 1 800 adresses e-mail.

**Points Clés :**

*   **Vulnérabilité exploitée :** Résurrection de domaines, où un domaine expiré lié à un compte PyPI est enregistré par un attaquant pour détourner le compte.
*   **Impact potentiel :** Attaques sur la chaîne d'approvisionnement logicielle via le détournement de paquets Python populaires.
*   **Mesure adoptée par PyPI :** Vérification quotidienne du statut d'expiration des domaines des adresses e-mail vérifiées et dé-vérification de celles associées à des domaines expirés.
*   **Outil utilisé :** API Status de Domainr pour le suivi du cycle de vie des domaines.

**Recommandations :**

*   Ajouter une adresse e-mail de secours d'un domaine non personnalisé pour éviter les interruptions.
*   Activer l'authentification à deux facteurs (2FA) sur le compte PyPI pour une protection accrue.

---
[Source](https://www.bleepingcomputer.com/news/security/pypi-now-blocks-domain-resurrection-attacks-used-for-hijacking-accounts/){:target="_blank"}
