---
title: 'WhatsApp device linking abused in account hijacking attacks'
date: 2025-12-18
permalink: /posts/2025/12/18/whatsapp-device-linking-abused-in-account-hijacking-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Usurpation de comptes WhatsApp via une fonctionnalité de liaison d'appareils**

Des acteurs malveillants exploitent la fonction légitime de liaison d'appareils de WhatsApp pour détourner des comptes, dans le cadre d'une campagne baptisée GhostPairing. Cette méthode ne nécessite aucune authentification préalable de la part de la victime, qui est trompée pour autoriser la connexion du navigateur de l'attaquant à son compte WhatsApp. Une fois cette liaison établie, les pirates obtiennent l'accès complet à l'historique des conversations et aux médias partagés, pouvant ainsi usurper l'identité de l'utilisateur ou commettre des fraudes.

**Fonctionnement de l'attaque GhostPairing :**

L'attaque débute par un message court, provenant d'un contact connu, partageant un lien prétendant mener à une photo en ligne de la victime. Ce lien est souvent présenté avec un aperçu de contenu Facebook pour renforcer la confiance. La victime est alors redirigée vers une fausse page Facebook, hébergée sur des domaines similaires à ceux de Facebook, l'invitant à se connecter pour vérifier son identité avant d'accéder au contenu.

Cette page de vérification déclenche en réalité le processus de liaison d'appareil de WhatsApp. La victime est invitée à saisir son numéro de téléphone, utilisé par l'attaquant pour initier une demande de liaison légitime. WhatsApp génère alors un code d'appairage que l'attaquant affiche sur sa fausse page. La victime, incitée à entrer ce code pour "finaliser la connexion", autorise ainsi la liaison de l'appareil de l'attaquant à son compte.

Bien que WhatsApp alerte l'utilisateur lors d'une tentative de liaison d'un nouvel appareil, cette notification est souvent négligée. L'accès à WhatsApp Web permet alors à l'attaquant de consulter les messages en temps réel, de télécharger des médias, d'envoyer de nouveaux messages et de propager le même leurre à ses contacts.

**Points clés :**

*   **Exploitation de la fonction de liaison d'appareils :** L'attaque cible spécifiquement la fonctionnalité permettant de connecter WhatsApp à d'autres appareils.
*   **Ingénierie sociale :** Les victimes sont trompées par des messages de contacts connus et des liens semblant légitimes.
*   **Faux sites de connexion :** Des pages d'apparence légitime incitent les victimes à révéler des informations ou des codes.
*   **Absence d'authentification directe :** L'attaquant n'a pas besoin de mots de passe ou de codes 2FA de la victime, il obtient un accès via la procédure de liaison.
*   **Diffusion rapide :** Les comptes compromis servent de tremplin pour atteindre de nouvelles victimes.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques pour cette attaque. La vulnérabilité réside dans la conception du processus de liaison d'appareils et la manière dont les utilisateurs peuvent être induits en erreur.

**Recommandations :**

*   **Vérifier les appareils connectés :** Se rendre dans les paramètres de WhatsApp (Paramètres → Appareils connectés) pour identifier et déconnecter tout appareil non autorisé.
*   **Activer l'authentification à deux facteurs :** Renforce la sécurité du compte, bien que non directement exploitable par cette méthode, elle protège contre d'autres formes de compromission.
*   **Être vigilant face aux messages suspects :** Prendre le temps d'analyser les messages, de vérifier leur légitimité et l'identité de l'expéditeur avant de cliquer sur des liens ou d'entrer des informations.
*   **Bloquer et signaler :** Les messages suspects doivent être signalés et les expéditeurs bloqués.

---
[Source](https://www.bleepingcomputer.com/news/security/whatsapp-device-linking-abused-in-account-hijacking-attacks/){:target="_blank"}
