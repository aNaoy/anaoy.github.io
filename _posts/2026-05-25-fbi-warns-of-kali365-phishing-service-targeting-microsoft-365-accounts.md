---
title: 'FBI warns of Kali365 phishing service targeting Microsoft 365 accounts'
date: 2026-05-25
permalink: /posts/2026/05/25/fbi-warns-of-kali365-phishing-service-targeting-microsoft-365-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Kali365 : La menace croissante du Phishing par code d'appareil

Le FBI a alerté sur l'émergence de **Kali365**, une plateforme de *Phishing-as-a-Service* (PhaaS) permettant à des cybercriminels peu qualifiés de pirater des comptes Microsoft 365 et Entra.

**Points clés :**
*   **Méthode d'attaque :** Utilisation détournée du flux d'autorisation OAuth 2.0 (conçu initialement pour les appareils IoT/TV connectées). L'attaquant génère un code d'appareil et incite la victime, via du phishing, à le valider sur le portail légitime de Microsoft.
*   **Contournement MFA :** Une fois le code validé par l'utilisateur, Microsoft délivre un jeton d'accès OAuth, offrant aux attaquants un accès total au compte, y compris aux applications SaaS (Salesforce, etc.), sans avoir à intercepter de code MFA.
*   **Double fonctionnalité :** Kali365 propose également un mode "Cookie Link" (Adversary-in-the-Middle) pour intercepter les jetons de session et cookies d'authentification après résolution du MFA.
*   **Services offerts :** La plateforme fournit des outils automatisés : leurres par IA, tableaux de bord de suivi en temps réel et modèles de campagnes.
*   **Conséquences :** Accès aux boîtes mail, création de règles de dissimulation, enregistrement de nouveaux appareils malveillants sur le réseau de la victime.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique (CVE), mais d'un **abus de conception légitime** du flux d'authentification OAuth 2.0 Device Authorization.

**Recommandations :**
*   **Accès Conditionnel :** Restreindre ou bloquer totalement les flux d'authentification par code d'appareil via les politiques d'accès conditionnel de Microsoft Entra.
*   **Audit :** Examiner l'usage actuel des codes d'appareil dans l'organisation et bloquer les politiques de transfert d'authentification entre appareils.
*   **Surveillance :** Surveiller les inscriptions de nouveaux appareils suspects et la création de règles de messagerie inhabituelles.
*   **Réaction :** En cas d'incident, conserver les preuves (e-mails de phishing, logs de connexion) et signaler l'intrusion aux autorités compétentes (type IC3).

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-warns-of-kali365-phishing-service-targeting-microsoft-365-accounts/){:target="_blank"}
