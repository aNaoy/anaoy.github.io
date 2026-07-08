---
title: 'New Ghost Phishing Wave Is Breaking Traditional Email Security'
date: 2026-07-08
permalink: /posts/2026/07/08/new-ghost-phishing-wave-is-breaking-traditional-email-security/
tags:
- veille-cyber
- hackernews
---
### La menace du "Ghost Phishing" : contournement des défenses email par chiffrement côté client

Les campagnes de type "EvilTokens" exploitent une technique de "ghost phishing" (hameçonnage fantôme) qui échappe aux outils de sécurité traditionnels. Le code malveillant reste invisible lors de l'analyse initiale de l'email, car son contenu HTML est chiffré (AES-GCM) et ne se déchiffre qu'une fois ouvert dans le navigateur de la victime.

**Points clés :**
*   **Méthode :** Utilisation du "Microsoft Device Code Phishing". L'attaquant n'a pas besoin de dérober le mot de passe ; il incite l'utilisateur à autoriser l'accès à son compte Microsoft 365 via un flux de connexion légitime.
*   **Vulnérabilité :** L'angle mort des solutions de sécurité réside dans le fait que les contrôles statiques (URL, scan réseau) n'interceptent pas le contenu dynamique rendu par le DOM du navigateur.
*   **Impact :** Compromission de comptes cloud, vol de données sensibles, et augmentation des coûts opérationnels liés à la réponse aux incidents en raison d'une visibilité incomplète.
*   **Secteurs visés :** Fort impact sur les services financiers, le conseil, l'industrie, l'éducation et les MSSP.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car la technique repose sur le détournement d'un flux d'authentification légitime de Microsoft (Device Code Flow) couplé à une obfuscation du code malveillant par chiffrement AES-GCM côté client.

**Recommandations :**
*   **Adopter une analyse en bac à sable (sandbox) interactive :** Utiliser des outils capables d'exécuter le code dans un navigateur pour observer le comportement dynamique (DOM, requêtes HTTP, déchiffrement).
*   **Améliorer la visibilité SOC :** Se concentrer sur l'inspection des données au niveau du navigateur pour obtenir des preuves concrètes (instantanés du DOM, endpoints de communication) plutôt que sur des scans de liens statiques.
*   **Automatisation :** Générer des rapports intégrant le contexte complet de l'attaque pour accélérer les décisions de confinement des équipes de niveau 1 vers le niveau 2.
*   **Hunting :** Utiliser les indicateurs de compromission (IOC) extraits de l'analyse dynamique pour renforcer la détection des infrastructures d'attaque associées.

---
[Source](https://thehackernews.com/2026/07/new-ghost-phishing-wave-is-breaking.html){:target="_blank"}
