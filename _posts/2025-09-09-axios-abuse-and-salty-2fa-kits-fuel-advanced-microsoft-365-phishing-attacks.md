---
title: 'Axios Abuse and Salty 2FA Kits Fuel Advanced Microsoft 365 Phishing Attacks'
date: 2025-09-09
permalink: /posts/2025/09/09/axios-abuse-and-salty-2fa-kits-fuel-advanced-microsoft-365-phishing-attacks/
tags:
- veille-cyber
- hackernews
---
**Évolution des Attaques de Phishing : Exploitation d'Axios et de kits "Salty 2FA" pour Contourner Microsoft 365**

Des acteurs malveillants exploitent désormais des outils tels qu'Axios, un client HTTP, en combinaison avec la fonctionnalité "Direct Send" de Microsoft 365. Cette synergie crée un pipeline d'attaque très efficace, visant à contourner les défenses et à voler des informations d'identification.

**Points Clés :**

*   **Augmentation de l'Utilisation d'Axios :** L'activité liée à l'agent utilisateur Axios a connu une croissance exponentielle (241%) entre juin et août 2025, représentant une part significative du trafic suspect. Sa polyvalence permet aux attaquants de l'utiliser pour intercepter, modifier et rejouer des requêtes HTTP, facilitant ainsi le vol de jetons de session ou de codes d'authentification multifacteur (MFA).
*   **Abus de "Direct Send" :** Les campagnes de phishing tirent parti de la fonction légitime "Direct Send" de Microsoft 365 pour usurper l'identité d'utilisateurs de confiance et distribuer des emails malveillants. Associée à Axios, cette méthode permet aux messages de passer plus facilement les passerelles de sécurité, atteignant ainsi les boîtes de réception des utilisateurs avec un taux de réussite de 70%.
*   **"Salty 2FA" :** Un nouveau service de phishing-as-a-service (PhaaS), nommé "Salty 2FA", a été identifié. Il est conçu pour voler des identifiants Microsoft et contourner la MFA en simulant diverses méthodes d'authentification (SMS, applications, appels, etc.).
*   **Tactiques d'Évasion Avancées :** Ces attaques intègrent des techniques sophistiquées comme le "geofencing", le filtrage d'adresses IP, la désactivation des outils de développement, et l'utilisation de sous-domaines dynamiques pour compliquer l'analyse et brouiller la distinction entre trafic légitime et malveillant. L'utilisation d'infrastructures comme Google Firebase et des pages d'atterrissage mimant des notifications légitimes (par exemple, OneDrive) renforce la tromperie.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée pour Axios ou "Direct Send" dans cet article. L'exploitation réside dans l'utilisation abusive de fonctionnalités légitimes et d'outils de développement par des acteurs malveillants.

**Recommandations :**

*   Sécuriser la fonctionnalité "Direct Send" de Microsoft 365 et la désactiver si elle n'est pas nécessaire.
*   Configurer des politiques anti-usurpation appropriées sur les passerelles de messagerie.
*   Former les employés à reconnaître les emails de phishing.
*   Bloquer les domaines suspects.
*   Surveiller l'activité suspecte liée aux agents utilisateurs comme Axios.
*   Être vigilant face aux simulations d'authentification multifacteur et aux pages de connexion qui imitent des portails d'entreprise.

---
[Source](https://thehackernews.com/2025/09/axios-abuse-and-salty-2fa-kits-fuel.html){:target="_blank"}
