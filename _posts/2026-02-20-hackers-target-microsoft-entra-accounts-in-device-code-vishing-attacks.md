---
title: 'Hackers target Microsoft Entra accounts in device code vishing attacks'
date: 2026-02-20
permalink: /posts/2026/02/20/hackers-target-microsoft-entra-accounts-in-device-code-vishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Nouvelle tactique de phishing : le "vishing" de code d'appareil pour usurper les comptes Microsoft Entra**

Des acteurs malveillants ciblent désormais les organisations technologiques, manufacturières et financières en combinant des tactiques de phishing de code d'appareil et de vishing (hameçonnage vocal). Ces attaques exploitent le flux d'autorisation de périphérique OAuth 2.0 pour compromettre les comptes Microsoft Entra.

Contrairement aux méthodes précédentes qui utilisaient des applications OAuth malveillantes, cette nouvelle approche emploie des identifiants clients OAuth légitimes de Microsoft et le flux d'autorisation de périphérique. Cela permet aux attaquants de tromper les victimes pour qu'elles s'authentifient, leur fournissant ainsi des jetons d'authentification valides. Ces jetons permettent d'accéder aux comptes des victimes sans avoir recours à des sites de phishing classiques ou à l'interception de codes MFA.

La bande d'extorsion ShinyHunters serait à l'origine de ces attaques, une affirmation non confirmée indépendamment mais précédemment associée à des attaques similaires contre Okta et Microsoft Entra.

**Points Clés :**

*   **Exploitation du flux d'autorisation de périphérique OAuth 2.0 :** Ce mécanisme, conçu pour faciliter la connexion d'appareils sans entrées clavier (IoT, imprimantes, téléviseurs), est détourné.
*   **Utilisation de codes "device_code" et "user_code" :** Les attaquants génèrent ces codes via des outils open-source et demandent aux victimes de les saisir sur la page de connexion Microsoft (microsoft.com/devicelogin).
*   **Authentification légitime trompeuse :** La victime s'authentifie normalement avec ses identifiants et passe la vérification MFA. L'application OAuth, qui peut être légitime, est ensuite autorisée.
*   **Obtention de jetons d'accès :** Une fois le flux complété, les attaquants récupèrent le jeton de rafraîchissement, qu'ils échangent contre des jetons d'accès. Ces derniers permettent de s'authentifier en tant que l'utilisateur sans nouvelle étape MFA.
*   **Accès aux applications SaaS connectées :** Les jetons d'accès octroient un accès aux services Microsoft 365 et autres applications configurées avec l'authentification unique (SSO) du locataire victime, facilitant le vol de données.

**Vulnérabilités :**

*   **Mélange du phishing de code d'appareil avec le vishing :** L'aspect vocal ajoute une pression sociale et une crédibilité accrue à la demande d'authentification.
*   **Abus d'un mécanisme d'authentification légitime :** Le flux d'autorisation de périphérique, conçu pour la commodité, est utilisé comme vecteur d'attaque.
*   **Confiance accordée aux applications OAuth légitimes :** L'utilisation d'identifiants clients Microsoft existants ou d'applications reconnues masque la nature malveillante de l'opération.

Aucun CVE spécifique n'est mentionné dans l'article pour cette méthode d'attaque.

**Recommandations :**

*   **Bloquer les domaines et adresses d'expéditeurs malveillants.**
*   **Auditer et révoquer les consentements d'applications OAuth suspects.**
*   **Examiner les journaux de connexion Azure AD à la recherche d'événements d'authentification de code d'appareil.**
*   **Désactiver l'option de flux de code d'appareil lorsque non nécessaire.**
*   **Mettre en place des politiques d'accès conditionnel robustes.**

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-microsoft-entra-accounts-in-device-code-vishing-attacks/){:target="_blank"}
