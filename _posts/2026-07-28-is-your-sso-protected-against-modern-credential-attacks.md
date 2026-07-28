---
title: 'Is Your SSO Protected Against Modern Credential Attacks?'
date: 2026-07-28
permalink: /posts/2026/07/28/is-your-sso-protected-against-modern-credential-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Sécuriser les accès SSO face aux menaces modernes

Le Single Sign-On (SSO) centralise l'authentification, simplifiant l'accès aux ressources, mais il constitue également un point de défaillance critique. La compromission d'un compte SSO unique peut permettre aux attaquants d'accéder à l'ensemble des systèmes connectés (VPN, applications SaaS, services internes), comme l'a illustré la violation de données de l'Université de Pennsylvanie en 2025.

**Points clés :**
*   **Centralisation du risque :** Un SSO mal protégé offre un accès transversal aux applications sensibles.
*   **Vulnérabilité des identifiants :** Les outils de type *infostealer* permettent de dérober des mots de passe, rendant les politiques de sécurité traditionnelles obsolètes.
*   **Nécessité d'une défense en profondeur :** La sécurité du SSO ne dépend pas seulement de l'activation du service, mais de la robustesse des mesures entourant l'identité.

**Vulnérabilités :**
Bien que l'article ne liste pas de CVE spécifiques, il souligne les faiblesses structurelles suivantes :
*   **Faiblesse des politiques de mots de passe :** Utilisation de règles de complexité obsolètes (changements fréquents) qui favorisent des mots de passe prévisibles.
*   **MFA inadaptée :** L'usage de méthodes vulnérables au phishing (codes SMS ou OTP basiques).
*   **Gestion des jetons et secrets :** Mauvaise protection des secrets OAuth, des clés de signature de jetons (SAML) et des permissions excessives accordées aux applications tierces.

**Recommandations :**
*   **Politique de mots de passe moderne :** Privilégier la longueur (au moins 15 caractères sans MFA, 8 avec MFA) et comparer les nouveaux mots de passe à des listes de compromissions connues (ex: NIST).
*   **Authentification résistante au phishing :** Implémenter des méthodes basées sur FIDO2, WebAuthn ou des clés de sécurité, particulièrement pour les comptes à privilèges.
*   **Sécurisation de l'IdP (Fournisseur d'Identité) :** Protéger les comptes administrateurs via un accès *Just-In-Time* et une surveillance étroite.
*   **Gestion stricte des assets :** Stocker les secrets dans des coffres-forts, faire pivoter régulièrement les clés de signature et révoquer les permissions (consentements) inutilisées ou trop larges des applications tierces.

---
[Source](https://www.bleepingcomputer.com/news/security/is-your-sso-protected-against-modern-credential-attacks/){:target="_blank"}
