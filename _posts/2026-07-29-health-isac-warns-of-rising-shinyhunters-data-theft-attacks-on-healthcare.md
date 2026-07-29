---
title: 'Health-ISAC warns of rising ShinyHunters data theft attacks on healthcare'
date: 2026-07-29
permalink: /posts/2026/07/29/health-isac-warns-of-rising-shinyhunters-data-theft-attacks-on-healthcare/
tags:
- veille-cyber
- bleepingcomp
---
### Menace accrue du groupe ShinyHunters sur le secteur de la santé

Le Health-ISAC alerte sur une intensification des attaques du groupe cybercriminel ShinyHunters ciblant le secteur de la santé. Ce groupe se spécialise dans le vol de données à grande échelle via des compromissions de plateformes SaaS et de stockage cloud, utilisant souvent les intégrations de la chaîne d'approvisionnement pour accéder aux jetons OAuth.

**Points clés :**
*   **Mode opératoire :** Les attaquants ciblent les employés par ingénierie sociale (vishing/phishing) pour compromettre des comptes Single Sign-On (SSO) comme Okta, Microsoft Entra ou Google.
*   **Vecteur d'attaque :** Utilisation de kits de phishing sophistiqués permettant des interactions en temps réel pour manipuler les helpdesks afin de réinitialiser des mots de passe ou des méthodes MFA.
*   **Objectif :** Une fois le compte SSO compromis, il sert de « centre de contrôle » pour accéder à l'ensemble des applications SaaS de l'entreprise (Salesforce, Microsoft 365, SharePoint, etc.) et exfiltrer massivement des données.
*   **Vulnérabilités :** L'absence de MFA résistant au phishing et des procédures de helpdesk permissives sont les failles principales exploitées. Aucun CVE spécifique n'est mentionné, car l'attaque repose sur une exploitation légitime des identités et des processus.

**Recommandations :**
*   **Sécurisation du Helpdesk :** Mettre en œuvre une politique « sans appel unique » : toute demande de réinitialisation doit faire l'objet d'un ticket et d'un rappel à un numéro vérifié (hors bande).
*   **Authentification :** Déployer des méthodes MFA résistantes au phishing (clés FIDO2/WebAuthn) pour les utilisateurs à haut risque et restreindre ou supprimer le MFA par SMS/voix.
*   **Gestion des accès :** Traiter les systèmes SSO comme des actifs « Tier 0 » (critiques). Appliquer des politiques d'accès conditionnel basées sur des appareils gérés et bloquer l'authentification héritée.
*   **Surveillance :** Centraliser les logs d'audit SaaS pour détecter les comportements anormaux : nouvelles inscriptions MFA, accès API inhabituels, téléchargements massifs de fichiers ou changements géographiques impossibles.
*   **Réponse :** S'assurer que les équipes de sécurité peuvent révoquer instantanément les sessions actives et supprimer les applications OAuth malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/health-isac-warns-of-rising-shinyhunters-data-theft-attacks-on-healthcare/){:target="_blank"}
