---
title: 'Chick-fil-A discloses data breach after credential stuffing attacks'
date: 2026-07-22
permalink: /posts/2026/07/22/chick-fil-a-discloses-data-breach-after-credential-stuffing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de comptes Chick-fil-A via « Credential Stuffing »

La chaîne de restauration Chick-fil-A a été victime d'une attaque par « credential stuffing » (bourrage d'identifiants) visant son site web et son application mobile entre le 17 et le 19 juin 2026. Des attaquants ont utilisé des identifiants (emails et mots de passe) dérobés lors de fuites de données antérieures sur d'autres plateformes pour accéder aux comptes « Chick-fil-A One ».

**Points clés :**
* **Méthode :** Utilisation d'outils automatisés testant massivement des couples identifiant/mot de passe compromis ailleurs.
* **Données exposées :** Noms, emails, numéros de membre, données de paiement mobile, codes QR, solde de crédits, les quatre derniers chiffres des cartes bancaires, et potentiellement adresses, numéros de téléphone et dates de naissance.
* **Impact :** Un nombre indéterminé de clients est touché, avec des signalements confirmés dans plusieurs États américains (ex: 2 182 personnes au Texas). Il s'agit du second incident majeur de ce type pour l'enseigne après celui de 2023.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique, car l'attaque repose sur la réutilisation d'identifiants par les utilisateurs plutôt que sur une faille logicielle de l'application. Cette vulnérabilité est structurelle : l'absence de protection contre le bourrage d'identifiants et l'usage de mots de passe identiques sur plusieurs services facilitent ces intrusions.

**Recommandations :**
* **Pour les utilisateurs :** Changer immédiatement le mot de passe du compte Chick-fil-A et, surtout, ne jamais réutiliser le même mot de passe sur plusieurs sites web. L'usage d'un gestionnaire de mots de passe est fortement conseillé.
* **Pour l'entreprise :** Mettre en œuvre des mesures de défense renforcées, telles que l'authentification multifacteur (MFA), la détection comportementale pour bloquer les tentatives de connexion automatisées, et la mise en place de systèmes de type « CAPTCHA » ou de monitoring de trafic pour identifier les attaques par force brute.

---
[Source](https://www.bleepingcomputer.com/news/security/chick-fil-a-discloses-data-breach-after-credential-stuffing-attacks/){:target="_blank"}
