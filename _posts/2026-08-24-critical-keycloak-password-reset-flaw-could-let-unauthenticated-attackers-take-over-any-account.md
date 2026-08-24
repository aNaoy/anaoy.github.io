---
title: 'Critical Keycloak Password Reset Flaw Could Let Unauthenticated Attackers Take Over Any Account'
date: 2026-08-24
permalink: /posts/2026/08/24/critical-keycloak-password-reset-flaw-could-let-unauthenticated-attackers-take-over-any-account/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de réinitialisation de mot de passe dans Keycloak

Une faille de sécurité critique a été découverte dans le serveur d'identité open-source Keycloak, permettant à un attaquant distant non authentifié de prendre le contrôle total de n'importe quel compte utilisateur, y compris les comptes administrateurs, sans aucune interaction requise.

**Points clés :**
*   **Cause racine :** Un défaut de validation d'état lors du flux de réinitialisation des identifiants (« reset-credentials »). Une requête spécifiquement conçue permet de contourner l'envoi du jeton d'action par e-mail et de passer directement à l'étape de définition d'un nouveau mot de passe.
*   **Impact :** Compromission complète de compte. Étant donné que Keycloak est souvent au cœur de l'infrastructure d'authentification, cette faille peut potentiellement donner accès à tous les services situés derrière le serveur.
*   **Statut :** Aucune preuve d'exploitation active n'a été recensée à ce jour.

**Vulnérabilité identifiée :**
*   **CVE-2026-18963 :** Classée 9.1 (Critique) selon le score CVSS. Catégorisée comme un mécanisme de récupération de mot de passe faible (CWE-640).

**Recommandations :**
*   **Mise à jour immédiate :**
    *   **Upstream Keycloak :** Passer à la version **26.7.2**.
    *   **Red Hat build of Keycloak (RHBK) :** Appliquer les correctifs pour les versions **26.4.15** ou **26.6.6**.
*   **Atténuation temporaire :** Si la mise à jour n'est pas réalisable immédiatement, désactiver la fonctionnalité « Mot de passe oublié » (« Forgot password ») dans les paramètres de connexion de chaque royaume (realm) de la console d'administration.

---
[Source](https://thehackernews.com/2026/08/critical-keycloak-password-reset-flaw.html){:target="_blank"}
