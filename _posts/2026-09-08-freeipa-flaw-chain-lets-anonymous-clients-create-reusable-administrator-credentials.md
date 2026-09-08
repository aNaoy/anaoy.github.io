---
title: 'FreeIPA Flaw Chain Lets Anonymous Clients Create Reusable Administrator Credentials'
date: 2026-09-08
permalink: /posts/2026/09/08/freeipa-flaw-chain-lets-anonymous-clients-create-reusable-administrator-credentials/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans FreeIPA : Risque d'usurpation d'identité administrateur

Des failles de sécurité majeures dans FreeIPA permettent à des utilisateurs non authentifiés de créer des identités Kerberos arbitraires et d'obtenir des privilèges d'administrateur.

#### Points clés
*   **Chaîne d'exploitation :** L'attaque combine une faille dans FreeIPA (gestion des accès) et une vulnérabilité dans 389 Directory Server (gestion des permissions).
*   **Impact :** Un attaquant peut créer un compte avec des identifiants réutilisables, rejoindre le groupe des administrateurs et, dans certains cas, accéder aux services HTTP et à l'autorité de certification (Dogtag).
*   **Risque environnemental :** Une seconde faille permet à tout utilisateur authentifié d'extraire des variables d'environnement, exposant potentiellement des mots de passe administrateur dans les déploiements par conteneurs.

#### Vulnérabilités identifiées
*   **CVE-2026-76578 (FreeIPA) :** Permet à un client non authentifié de créer une identité et d'accéder au groupe administrateur. (Score CVSS : 9.8)
*   **CVE-2026-76560 (389 Directory Server) :** Erreur dans le moteur de contrôle d'accès comparant les noms d'utilisateurs ; un client anonyme (nom vide) peut valider les contrôles de propriété. (Score CVSS : 7.5)
*   **CVE-2026-79678 (FreeIPA) :** Injection dans la commande `idp-add` via `eval()` permettant la fuite de variables d'environnement. (Score CVSS : 8.1)

#### Recommandations
*   **Mise à jour :** Installer **FreeIPA 4.13.4** dès que disponible. Appliquer les correctifs pour `389-ds-base` fournis par votre distribution (Red Hat, Fedora).
*   **Sécurisation réseau :** Restreindre l'accès aux ports LDAP (389 et 636) aux seules machines de confiance via pare-feu ou segmentation réseau.
*   **Configuration :** Désactiver les "binds" LDAP anonymes si les besoins du déploiement le permettent.
*   **Vérification (Conteneurs) :** Pour les déploiements par conteneurs, s'assurer que les mots de passe administrateurs initiaux ne sont plus présents dans les variables d'environnement après le démarrage.

---
[Source](https://thehackernews.com/2026/09/freeipa-flaw-chain-lets-anonymous.html){:target="_blank"}
