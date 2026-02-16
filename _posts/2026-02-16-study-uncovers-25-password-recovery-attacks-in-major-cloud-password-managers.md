---
title: 'Study Uncovers 25 Password Recovery Attacks in Major Cloud Password Managers'
date: 2026-02-16
permalink: /posts/2026/02/16/study-uncovers-25-password-recovery-attacks-in-major-cloud-password-managers/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilités dans les gestionnaires de mots de passe cloud**

Une étude a révélé que plusieurs gestionnaires de mots de passe basés sur le cloud, notamment Bitwarden, Dashlane et LastPass, sont vulnérables à diverses attaques permettant la récupération de mots de passe. Ces failles peuvent entraîner des violations d'intégrité ou un compromis total des coffres-forts. L'étude a identifié un total de 25 attaques distinctes réparties comme suit : 12 contre Bitwarden, 7 contre LastPass et 6 contre Dashlane. Ces services sont utilisés par plus de 60 millions d'utilisateurs et 125 000 entreprises.

**Points clés :**

*   L'étude s'est concentrée sur les promesses de chiffrement "zero-knowledge" (ZKE) des gestionnaires de mots de passe, dans un scénario où le serveur est malveillant.
*   Les vulnérabilités exploitent des erreurs de conception et des incompréhensions cryptographiques.
*   1Password a également été jugé vulnérable à certains types d'attaques, mais l'entreprise considère ces problèmes comme des limitations architecturales déjà connues.

**Vulnérabilités identifiées :**

Les attaques peuvent être regroupées en quatre catégories principales :

1.  **Exploitation du mécanisme de récupération de compte "Key Escrow" :** Vulnérabilités dans la conception de la conservation des clés chez Bitwarden et LastPass, compromettant la confidentialité.
2.  **Exploitation du chiffrement d'éléments défectueux :** Chiffrement séparé des données et des paramètres, combiné à des métadonnées non chiffrées ou non authentifiées. Cela peut entraîner des violations d'intégrité, des fuites de métadonnées, l'échange de champs et des dégradations de la fonction de dérivation de clé (KDF).
3.  **Exploitation des fonctionnalités de partage :** Compromission de l'intégrité et de la confidentialité des coffres-forts via les fonctions de partage.
4.  **Exploitation de la rétrocompatibilité avec du code hérité :** Attaques de dégradation (downgrade) chez Bitwarden et Dashlane.

*   Aucun CVE spécifique n'est mentionné dans l'article pour ces vulnérabilités.

**Recommandations et mesures prises :**

*   **Dashlane :** A corrigé une vulnérabilité (identifiée par Dashlane comme une "cryptography downgrade issue" avec la version 6.2544.1 de son extension) qui permettait une dégradation du modèle de chiffrement utilisé pour générer les clés de chiffrement et protéger les coffres-forts. Cette correction a été réalisée en supprimant le support des méthodes cryptographiques héritées.
*   **Bitwarden :** Indique que sept des problèmes identifiés ont été résolus ou sont en cours de résolution. Les trois autres problèmes ont été acceptés comme des décisions de conception intentionnelles nécessaires au fonctionnement du produit.
*   **LastPass :** Travaille activement à l'ajout de garanties d'intégrité plus solides pour mieux lier cryptographiquement les éléments, les champs et les métadonnées. Ils prévoient également de renforcer leurs flux de réinitialisation de mot de passe administrateur et de partage.
*   **1Password :** Affirme que son architecture de sécurité a été évaluée et qu'aucun nouveau vecteur d'attaque n'a été découvert au-delà de ceux déjà documentés dans leur livre blanc sur la conception de la sécurité. Ils utilisent notamment le protocole Secure Remote Password (SRP) pour l'authentification des utilisateurs.

Pour le moment, il n'y a aucune preuve que ces problèmes aient été exploités dans la nature.

---
[Source](https://thehackernews.com/2026/02/study-uncovers-25-password-recovery.html){:target="_blank"}
