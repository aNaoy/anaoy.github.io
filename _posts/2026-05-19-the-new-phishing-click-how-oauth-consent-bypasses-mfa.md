---
title: 'The New Phishing Click: How OAuth Consent Bypasses MFA'
date: 2026-05-19
permalink: /posts/2026/05/19/the-new-phishing-click-how-oauth-consent-bypasses-mfa/
tags:
- veille-cyber
- hackernews
---
### L’usurpation des autorisations OAuth : le nouveau vecteur d’attaque contournant l’authentification multifacteur (MFA)

Le phishing par consentement (ou abus de droits OAuth) représente une menace croissante qui supplante le phishing traditionnel. Contrairement au vol d'identifiants classiques, cette méthode incite l'utilisateur à accorder des permissions légitimes à une application malveillante via un écran de consentement OAuth, rendant le MFA inopérant puisqu'il a été validé lors du processus initial.

**Points clés :**
* **Fonctionnement :** L'attaquant obtient un jeton d'accès (« refresh token ») persistant et scoped (limité à certains droits comme la lecture d'e-mails ou de fichiers) qui reste valide même après un changement de mot de passe.
* **Invisibilité pour le SIEM :** Comme l'accès est autorisé par le système lui-même et ne nécessite pas de rejeu de mot de passe, l'activité ne déclenche aucune alerte de connexion suspecte.
* **Combinatoires toxiques :** Le risque majeur réside dans la multiplication des autorisations accordées à des agents IA, des intégrations ou des extensions, créant des ponts invisibles entre plusieurs applications SaaS sans autorisation centralisée.
* **Vulnérabilité structurelle :** Le manque de vigilance sur le « clic de consentement », normalisé par l'usage intensif d'outils tiers, permet aux attaquants de s'insérer sous la couche de sécurité périmétrique.

**Vulnérabilités :**
* Pas de CVE spécifique mentionnée (il s'agit d'un abus de conception de protocole et non d'un bug logiciel).
* Risque inhérent au mécanisme **OAuth Device Code Flow** détourné pour l'hameçonnage.

**Recommandations :**
* **Inventaire continu :** Maintenir une cartographie en temps réel de tous les jetons OAuth actifs et des permissions accordées.
* **Politiques de consentement :** Implémenter des politiques d'accès conditionnel qui exigent un re-consentement régulier (tous les 30 jours par exemple).
* **Surveillance des bridges :** Identifier et auditer les intégrations et agents IA qui connectent entre eux plusieurs systèmes SaaS, particulièrement ceux accédant à des données critiques.
* **Réponse sur mesure :** Développer des procédures de remédiation permettant de révoquer un jeton OAuth spécifique plutôt que de suspendre l'ensemble du compte utilisateur.
* **Automatisation :** Utiliser des plateformes de sécurité SaaS (ex: Reco) capables de détecter les abus de jetons et les combinaisons toxiques dans le graphe d'identité de l'organisation.

---
[Source](https://thehackernews.com/2026/05/the-new-phishing-click-how-oauth.html){:target="_blank"}
