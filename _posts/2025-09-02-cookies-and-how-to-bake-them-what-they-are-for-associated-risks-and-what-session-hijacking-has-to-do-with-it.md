---
title: 'Cookies and how to bake them: what they are for, associated risks, and what session hijacking has to do with it'
date: 2025-09-02
permalink: /posts/2025/09/02/cookies-and-how-to-bake-them-what-they-are-for-associated-risks-and-what-session-hijacking-has-to-do-with-it/
tags:
- veille-cyber
- securelist
---
## Comprendre et Sécuriser les Cookies Web

Les cookies sont de petits fichiers texte envoyés par un serveur web à votre navigateur, puis renvoyés à chaque visite ultérieure. Ils servent à identifier les utilisateurs, à améliorer l'expérience de navigation et à stocker diverses informations, telles que les préférences, les articles dans un panier ou les identifiants de session (Session ID). Les lois comme le RGPD imposent aux sites web d'informer les utilisateurs de la collecte de cookies et de leur permettre de gérer leurs préférences.

### Types de Cookies

Les cookies peuvent être classés selon plusieurs critères :

*   **Stockage temporel :**
    *   **Temporaires (ou de session) :** Valides uniquement pendant la session de navigation et supprimés à sa fin. Ils facilitent la navigation sans redemander de connexion ou de paramètres.
    *   **Persistants :** Restent sur l'appareil même après la fermeture du navigateur, avec une date d'expiration définie par le site. Ils sont souvent utilisés pour mémoriser les identifiants ou les préférences.
*   **Source :**
    *   **Première partie :** Créés par le site web visité, généralement pour son bon fonctionnement ou l'analyse.
    *   **Tiers :** Créés par d'autres sites, souvent pour la publicité ou l'analyse (ex: Google Analytics), et peuvent suivre l'activité sur plusieurs sites.
*   **Importance :**
    *   **Requis (essentiels) :** Nécessaires au fonctionnement de base du site, comme la gestion du panier ou la sécurité. Ils incluent souvent l'identifiant de session.
    *   **Optionnels :** Utilisés pour le marketing, l'analyse ou la performance. Ils peuvent collecter des données pour créer des profils d'utilisateurs, potentiellement sensibles.

Des technologies comme les "supercookies" ou "evercookies" utilisent des méthodes de stockage non standard pour rendre leur suppression plus difficile.

### Risques Associés et Vulnérabilités

Les données sensibles stockées dans les cookies, en particulier l'identifiant de session, sont des cibles privilégiées pour les cybercriminels. Les principales menaces incluent :

*   **Détournement de session (Session Hijacking) :** Permet à un attaquant de se faire passer pour un utilisateur légitime en volant son identifiant de session. Les méthodes incluent :
    *   **Session Sniffing :** Interception du trafic non chiffré (HTTP) pour voler les cookies.
    *   **Cross-Site Scripting (XSS) :** Injection de scripts malveillants dans les pages web pour accéder aux cookies de l'utilisateur.
    *   **Session Fixation :** L'attaquant force l'utilisation d'un identifiant de session préétabli par la victime.
    *   **Cross-Site Request Forgery (CSRF) :** Exploitation de la confiance du site dans le navigateur pour forcer des actions non désirées.
    *   **Attaques Man-in-the-Middle (MitM) :** Interception et potentielle modification du trafic entre l'utilisateur et le site.
    *   **IDs de Session Prévisibles :** Prédiction d'identifiants de session générés par des algorithmes faibles.
    *   **Cookie Tossing :** Exploitation de la gestion des cookies par sous-domaines pour injecter des cookies malveillants.
*   **Collecte de données personnelles :** Les cookies optionnels peuvent révéler des informations sur les habitudes de navigation, permettant de créer des profils détaillés et d'être utilisés pour le phishing ou le chantage.

### Recommandations de Sécurité

**Pour les développeurs :**

*   **Chiffrement du trafic :** Utiliser systématiquement HTTPS et HSTS pour forcer l'utilisation de connexions sécurisées.
*   **Protection contre XSS :** Valider et échapper les entrées utilisateur, utiliser des politiques de sécurité de contenu (CSP).
*   **Sécurisation des Cookies :**
    *   Utiliser les attributs `Secure` (pour HTTPS) et `HttpOnly` (pour empêcher l'accès par JavaScript).
    *   Mettre en place `SameSite=Lax` ou `Strict` pour prévenir le CSRF.
    *   Générer des identifiants de session uniques, aléatoires et cryptographiquement sécurisés.
    *   Changer l'identifiant de session après l'authentification.
    *   Utiliser des tokens CSRF uniques.
    *   Privilégier les préfixes `__Host-` pour les cookies afin d'éviter les attaques par cookie tossing.
*   **Gestion des sous-domaines :** Effectuer des audits réguliers et isoler le contenu généré par les utilisateurs.
*   **Alternatives aux cookies :** Envisager l'API Web Storage (localStorage, sessionStorage) ou des approches côté serveur pour une meilleure sécurité.

**Pour les utilisateurs :**

*   **Vérifier HTTPS :** S'assurer que le site utilise HTTPS et que le certificat est valide.
*   **Respecter les avertissements de sécurité :** Ne pas ignorer les alertes du navigateur concernant les certificats ou les connexions non sécurisées.
*   **Mettre à jour le navigateur :** Installer régulièrement les mises à jour pour bénéficier des correctifs de sécurité.
*   **Effacer régulièrement les données de navigation :** Supprimer les cookies et le cache.
*   **Utiliser l'authentification à deux facteurs :** Renforcer la sécurité des comptes.
*   **Gérer les préférences de cookies :** Refuser les cookies non essentiels lorsque cela est possible.
*   **Être vigilant avec les liens :** Vérifier les URL avant de cliquer, en particulier celles contenant des paramètres étranges.
*   **Sécuriser la connexion Wi-Fi :** Utiliser un VPN sur les réseaux publics.

---
[Source](https://securelist.com/cookies-and-session-hijacking/117390/){:target="_blank"}
