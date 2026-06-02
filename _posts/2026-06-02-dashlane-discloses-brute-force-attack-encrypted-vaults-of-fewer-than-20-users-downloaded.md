---
title: 'Dashlane Discloses Brute-Force Attack, Encrypted Vaults of Fewer Than 20 Users Downloaded'
date: 2026-06-02
permalink: /posts/2026/06/02/dashlane-discloses-brute-force-attack-encrypted-vaults-of-fewer-than-20-users-downloaded/
tags:
- veille-cyber
- hackernews
---
### Incident de sécurité : Attaque par force brute sur Dashlane

Le gestionnaire de mots de passe Dashlane a été la cible d'une attaque par force brute visant à contourner l'authentification à deux facteurs (2FA) et à enregistrer de nouveaux appareils sur des comptes existants. Bien que les systèmes internes de l'entreprise n'aient pas été compromis, les attaquants ont réussi à télécharger les coffres-forts chiffrés de moins de 20 utilisateurs particuliers.

**Points clés :**
* **Nature de l'attaque :** Attaque par force brute ciblée.
* **Impact limité :** Moins de 20 comptes personnels ont vu leurs données (coffres-forts chiffrés) exfiltrées.
* **Intégrité des données :** Les coffres-forts restent protégés par le mot de passe maître de l'utilisateur. Aucune donnée n'est exploitable sans celui-ci, à condition qu'il soit complexe.
* **Réaction :** Dashlane a notifié individuellement les utilisateurs concernés et a suspendu temporairement les comptes visés par un volume anormal de tentatives de connexion.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cet incident, l'attaque reposant sur une tentative de contournement des mécanismes d'authentification (brute-force) plutôt que sur une faille logicielle connue.

**Recommandations :**
* **Renforcement du mot de passe maître :** Utiliser une phrase secrète longue, unique et difficile à deviner.
* **Audit de sécurité :** Vérifier régulièrement la liste des appareils autorisés dans les paramètres du compte et supprimer tout appareil inconnu.
* **Authentification forte :** S'assurer que la double authentification (2FA) est activée pour renforcer la protection contre les accès non autorisés.

---
[Source](https://thehackernews.com/2026/06/dashlane-discloses-brute-force-attack.html){:target="_blank"}
