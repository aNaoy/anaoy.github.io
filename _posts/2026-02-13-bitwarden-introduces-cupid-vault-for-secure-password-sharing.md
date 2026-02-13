---
title: 'Bitwarden introduces ‘Cupid Vault’ for secure password sharing'
date: 2026-02-13
permalink: /posts/2026/02/13/bitwarden-introduces-cupid-vault-for-secure-password-sharing/
tags:
- veille-cyber
- bleepingcomp
---
### Partage sécurisé de mots de passe avec Bitwarden

Bitwarden a introduit une nouvelle fonctionnalité nommée "Cupid Vault" permettant aux utilisateurs de partager des identifiants de manière sécurisée avec d'autres utilisateurs via leur adresse e-mail. Cette option est accessible gratuitement et permet de créer une organisation à deux personnes pour gérer des collections de mots de passe.

La mise en place s'effectue via l'interface web de Bitwarden, où un propriétaire de compte peut inviter un second membre en ajoutant son e-mail. Pour se prémunir contre les attaques de type "man-in-the-middle", une phrase d'empreinte permet de vérifier l'identité du membre invité. Le coffre-fort partagé est entièrement isolé du coffre personnel. L'accès peut être révoqué à tout moment, et le partage peut être configuré dans les deux sens.

Il est à noter que la propriété des éléments partagés n'est pas liée à leur créateur, puisque les deux membres de l'organisation peuvent modifier ou supprimer des entrées. Cette fonctionnalité est cependant limitée à deux collections et deux utilisateurs pour les comptes gratuits. Les plans payants (Family, Teams, Enterprise) disposent déjà de fonctionnalités de partage plus avancées.

**Points clés :**

*   Introduction de "Cupid Vault" par Bitwarden pour un partage sécurisé de mots de passe.
*   Fonctionnalité gratuite pour tous les utilisateurs de Bitwarden.
*   Permet la création d'une "Organisation" à deux membres pour le partage.
*   Les mots de passe partagés sont stockés dans un coffre-fort isolé du coffre personnel.
*   Possibilité de vérifier l'identité de l'invité via une phrase d'empreinte.
*   Gestion centralisée et révocable des accès.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article.

**Recommandations :**

*   Utiliser la phrase d'empreinte pour vérifier l'identité du membre invité afin de prévenir les attaques.
*   Gérer attentivement les permissions et révoquer l'accès si nécessaire.
*   Comprendre que la fonctionnalité gratuite "Cupid Vault" est limitée à 2 utilisateurs et 2 collections.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-introduces-cupid-vault-for-secure-password-sharing/){:target="_blank"}
