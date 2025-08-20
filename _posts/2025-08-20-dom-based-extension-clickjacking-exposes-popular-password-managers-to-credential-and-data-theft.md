---
title: 'DOM-Based Extension Clickjacking Exposes Popular Password Managers to Credential and Data Theft'
date: 2025-08-20
permalink: /posts/2025/08/20/dom-based-extension-clickjacking-exposes-popular-password-managers-to-credential-and-data-theft/
tags:
- veille-cyber
- hackernews
---
**Usurpation de clics sur les extensions de gestionnaires de mots de passe : un risque de vol de données**

Une nouvelle technique d'attaque par usurpation de clics, baptisée "DOM-Based Extension Clickjacking", peut être utilisée pour voler des identifiants de connexion, des codes d'authentification à deux facteurs (2FA) et des informations de carte bancaire via des extensions de navigateurs populaires.

Cette vulnérabilité, présentée par le chercheur indépendant Marek Tóth, exploite la manipulation des éléments de l'interface utilisateur injectés dans le DOM par les extensions. En rendant ces éléments invisibles (par exemple, des formulaires de connexion), un site web malveillant peut inciter l'utilisateur à cliquer, déclenchant ainsi l'auto-remplissage des informations sensibles par le gestionnaire de mots de passe, qui sont ensuite envoyées à un serveur distant.

**Points clés :**

*   L'attaque peut permettre le vol de données sensibles (identifiants, 2FA, cartes bancaires) en un seul clic.
*   Les gestionnaires de mots de passe peuvent remplir des informations non seulement sur le domaine principal, mais aussi sur tous les sous-domaines.
*   La technique est généralisable à d'autres types d'extensions.
*   11 extensions de gestionnaires de mots de passe populaires ont été identifiées comme vulnérables, cumulées par des millions d'utilisateurs.

**Vulnérabilités :**

*   Les vulnérabilités spécifiques n'ont pas encore reçu de CVEs officielles, mais une demande a été faite auprès de l'US-CERT.
*   Des versions spécifiques des extensions ont été mentionnées comme étant affectées :
    *   1Password Password Manager 8.11.4.27
    *   Apple iCloud Passwords 3.1.25
    *   Bitwarden Password Manager 2025.7.0
    *   Enpass 6.11.6
    *   LastPass 4.146.3
    *   LogMeOnce 7.12.4

**Recommandations :**

*   Désactiver la fonction d'auto-remplissage dans les gestionnaires de mots de passe et utiliser la fonction copier-coller uniquement.
*   Pour les utilisateurs de navigateurs basés sur Chromium, configurer l'accès des sites aux extensions sur "on click" pour contrôler manuellement la fonctionnalité d'auto-remplissage.
*   Les éditeurs concernés travaillent sur des correctifs, mais certains les ont marqués comme informatifs. Il est donc crucial pour les utilisateurs d'appliquer les recommandations de sécurité en attendant les mises à jour.

---
[Source](https://thehackernews.com/2025/08/dom-based-extension-clickjacking.html){:target="_blank"}
