---
title: 'Hackers target Microsoft Entra accounts in device code vishing attacks'
date: 2026-02-19
permalink: /posts/2026/02/19/hackers-target-microsoft-entra-accounts-in-device-code-vishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
## Vishing et Code d'Appareil : Nouvelle Méthode d'Attaque contre Microsoft Entra

Des acteurs malveillants ciblent désormais des organisations des secteurs de la technologie, de la fabrication et de la finance en combinant le hameçonnage par code d'appareil et le vishing (hameçonnage vocal). L'objectif est d'exploiter le flux d'autorisation d'appareil OAuth 2.0 pour compromettre les comptes Microsoft Entra. Contrairement aux attaques précédentes qui utilisaient des applications OAuth malveillantes, cette nouvelle approche exploite des identifiants clients OAuth légitimes de Microsoft et le processus d'autorisation d'appareil pour tromper les victimes.

Cela permet aux attaquants d'obtenir des jetons d'authentification valides pour accéder aux comptes des victimes sans avoir recours à des sites de phishing traditionnels qui volent des mots de passe ou interceptent des codes d'authentification multifacteur. Le gang d'extorsion ShinyHunters est suspecté d'être derrière ces attaques, ayant déjà été lié à des attaques similaires contre Okta et Microsoft Entra.

### Points Clés :

*   **Combinaison Vishing et Hameçonnage par Code d'Appareil :** Utilisation d'appels téléphoniques pour inciter les victimes à utiliser un code d'authentification sur une page légitime de Microsoft.
*   **Exploitation du Flux d'Autorisation d'Appareil OAuth 2.0 :** Le mécanisme légitime conçu pour faciliter la connexion d'appareils sans interface utilisateur est détourné.
*   **Utilisation d'Identifiants Clients OAuth Légitimes :** Les attaquants emploient des `client_id` d'applications OAuth existantes, y compris celles de Microsoft.
*   **Obtention de Jetons d'Authentification Valides :** L'authentification de la victime, y compris potentiellement l'authentification multifacteur, permet aux attaquants d'obtenir des jetons d'accès et de rafraîchissement.
*   **Accès aux Applications SSO :** Une fois le jeton obtenu, les attaquants peuvent accéder à une multitude d'applications connectées via l'authentification unique (SSO) de la victime, telles que Microsoft 365, Salesforce, Google Workspace, et d'autres.
*   **Vol de Données pour Extorsion :** L'accès aux comptes compromis permet le vol de données d'entreprise.

### Vulnérabilités :

L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. La méthode d'attaque repose sur l'exploitation d'une fonctionnalité légitime du flux OAuth 2.0.

### Recommandations :

*   **Bloquer les Domaines et Adresses d'Expédition Malveillants :** Identifier et interdire les sources connues d'attaques.
*   **Auditer et Révoquer les Consentements d'Applications OAuth Suspectes :** Examiner les applications ayant accès aux comptes et supprimer celles qui ne sont pas nécessaires ou reconnues.
*   **Examiner les Journaux de Connexion Azure AD :** Rechercher les événements d'authentification par code d'appareil suspects.
*   **Désactiver le Flux d'Autorisation d'Appareil lorsque Non Requis :** Si le flux de code d'appareil n'est pas utilisé par l'organisation, il est recommandé de le désactiver.
*   **Appliquer des Politiques d'Accès Conditionnel :** Mettre en place des contrôles supplémentaires pour sécuriser l'accès aux ressources.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-microsoft-entra-accounts-in-device-code-vishing-attacks/){:target="_blank"}
