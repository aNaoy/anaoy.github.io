---
title: 'Rogue external MFA providers can steal passwords during logins'
date: 2026-09-23
permalink: /posts/2026/09/23/rogue-external-mfa-providers-can-steal-passwords-during-logins/
tags:
- veille-cyber
- bleepingcomp
---
### TrustSink : Vol de mots de passe via des fournisseurs MFA externes malveillants

La technique « TrustSink », découverte par Varonis Threat Labs, permet à un attaquant disposant de privilèges élevés d'enregistrer un fournisseur d'authentification multifacteur (MFA) externe malveillant au sein de Microsoft Entra. Ce dispositif intercepte le flux de connexion légitime pour dérober les mots de passe des utilisateurs en toute transparence.

**Points clés**
*   **Fonctionnement :** Lorsqu'un utilisateur tente de se connecter, Entra redirige le flux vers le fournisseur MFA externe. L'attaquant présente alors une fausse page de saisie de mot de passe imitant parfaitement Microsoft.
*   **Persistance :** Une fois le mot de passe capturé, le fournisseur malveillant envoie un jeton de succès à Entra, permettant à la connexion de se finaliser sans erreur. 
*   **Impact :** Même après une réinitialisation de mot de passe par l'utilisateur, le fournisseur malveillant reste actif dans la politique d'authentification et recapture le nouveau mot de passe lors de la tentative suivante.
*   **Prérequis :** L'attaque n'est pas un vecteur d'accès initial. Elle nécessite un compromis préalable avec des droits d'administrateur (Global Administrator ou Authentication Policy Administrator).

**Vulnérabilités**
*   Il s'agit d'un abus de conception logique dans la gestion des fournisseurs d'authentification externes (EAM) de Microsoft Entra, et non d'une CVE spécifique. L'attaque exploite la confiance implicite accordée par Entra aux jetons signés provenant de fournisseurs enregistrés.

**Recommandations**
*   **Remédiation immédiate :** Avant toute réinitialisation de mot de passe, identifier et supprimer les fournisseurs MFA externes suspects, ainsi que leurs applications et clés associées.
*   **Surveillance :** Auditer régulièrement les modifications apportées à la politique des méthodes d'authentification (*Authentication Methods Policy*).
*   **Gestion des privilèges :** Restreindre strictement les accès aux rôles d'administrateur global et d'administrateur de politique d'authentification.
*   **Durcissement :** Privilégier l'usage de méthodes d'authentification résistantes au phishing, telles que FIDO2 ou Windows Hello for Business, qui ne sont pas affectées par ce type de détournement.

---
[Source](https://www.bleepingcomputer.com/news/security/rogue-external-mfa-providers-can-steal-passwords-during-logins/){:target="_blank"}
