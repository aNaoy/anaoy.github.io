---
title: 'CISA and NSA share tips on securing Microsoft Exchange servers'
date: 2025-10-30
permalink: /posts/2025/10/30/cisa-and-nsa-share-tips-on-securing-microsoft-exchange-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Sécuriser Microsoft Exchange : Recommandations Essentielles**

Les agences de cybersécurité CISA et NSA, en collaboration avec leurs partenaires internationaux, ont publié des directives visant à renforcer la sécurité des serveurs Microsoft Exchange. Ces recommandations s'adressent aux administrateurs IT pour les protéger contre les cyberattaques.

**Points Clés et Recommandations :**

*   **Renforcer l'Authentification et l'Accès :**
    *   Implémenter l'authentification multifacteur (MFA) et l'authentification moderne (Modern Auth).
    *   Utiliser OAuth 2.0 pour une authentification sécurisée.
    *   Déployer Kerberos et SMB au lieu de NTLM.
    *   Restreindre l'accès administratif aux postes de travail autorisés.
    *   Mettre en place un contrôle d'accès basé sur les rôles (RBAC).
    *   Adopter les principes du modèle de sécurité "zero trust" (ZT).

*   **Minimiser la Surface d'Attaque :**
    *   Maintenir les serveurs à jour avec les derniers correctifs.
    *   Désactiver les services non essentiels.
    *   Activer les fonctionnalités intégrées de protection contre le spam et les logiciels malveillants.
    *   Configurer les "Download Domains" pour prévenir les attaques de Cross-Site Request Forgery (CSRF).
    *   Mettre en œuvre des configurations strictes pour le transport.

*   **Assurer un Chiffrement Réseau Robuste :**
    *   Configurer le Transport Layer Security (TLS) pour garantir l'intégrité des données.
    *   Activer la protection étendue (Extended Protection) pour se défendre contre les attaques de type Adversary-in-the-Middle (AitM), de relais et de transfert.
    *   Activer la signature basée sur les certificats pour la console de gestion Exchange (Exchange Management Shell).
    *   Implémenter HTTP Strict Transport Security (HSTS) pour sécuriser les connexions aux navigateurs.

*   **Gestion des Versions et Migration :**
    *   Migrer des versions obsolètes et non supportées d'Exchange vers Microsoft 365.
    *   Désactiver les serveurs Exchange locaux ou hybrides qui ne sont plus mis à jour, car ils représentent un risque de sécurité significatif.

*   **Surveillance et Réponse :**
    *   Surveiller les activités suspectes ou malveillantes.
    *   Planifier les incidents potentiels et les procédures de récupération.
    *   Surveiller les tentatives de manipulation de l'en-tête P2 FROM pour prévenir l'usurpation d'expéditeur.

**Vulnérabilités Mentionnées :**

*   **CVE-2025-53786 :** Une vulnérabilité critique affectant Microsoft Exchange Server 2016, 2019 et Subscription Edition. Elle permet aux attaquants obtenant un accès administratif sur des serveurs locaux de se déplacer latéralement vers des environnements cloud Microsoft, potentiellement menant à une compromission totale du domaine.
*   **ProxyShell et ProxyLogon :** Des failles de sécurité exploitées par des groupes d'attaquants parrainés par des États et des groupes criminels pour compromettre des serveurs Exchange.

Il est fortement recommandé aux organisations de prendre des mesures proactives pour atténuer ces risques et prévenir les activités malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-and-nsa-share-tips-on-securing-microsoft-exchange-servers/){:target="_blank"}
