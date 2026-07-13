---
title: 'Misconfigured Server Reveals Three Evilginx Phishing Operations Targeting Microsoft 365'
date: 2026-07-13
permalink: /posts/2026/07/13/misconfigured-server-reveals-three-evilginx-phishing-operations-targeting-microsoft-365/
tags:
- veille-cyber
- hackernews
---
### Compromission de serveurs et prolifération des campagnes de phishing Evilginx

Une faille de configuration sur un serveur (listing de répertoire activé) a permis à des chercheurs en sécurité de mettre au jour trois campagnes de phishing ciblant Microsoft 365. Ces opérations, menées par des acteurs utilisant le framework open-source **Evilginx**, exploitent deux méthodes distinctes pour contourner l'authentification multifacteur (MFA).

#### Points clés
*   **Infrastructure vulnérable :** Une simple commande `python3 -m http.server` laissée active a exposé des kits de phishing, des logs de récolte d'identifiants, des sessions Telegram et des outils d'administration à distance (RMM).
*   **Diversité des attaques :** Les attaquants utilisent des variantes d'Evilginx (proxy AiTM - Adversary-in-the-Middle) ou abusent du flux légitime de connexion par code d'appareil (OAuth device code flow).
*   **Assistance par IA :** Les attaquants ont largement utilisé des modèles de langage (Claude, API "uncensored") pour générer le code "glue" entourant leurs scripts de phishing.
*   **Écosystème :** Ces campagnes s'inscrivent dans une tendance de "Phishing-as-a-Service" (ex: "The Quarry"), où le seuil d'entrée pour lancer des attaques sophistiquées est devenu quasi nul.

#### Vulnérabilités exploitées
*   **AiTM (Adversary-in-the-Middle) :** Interception des jetons de session en temps réel, permettant de contourner les méthodes MFA classiques.
*   **OAuth Device Code Flow Abuse :** Abus d'un flux d'authentification légitime. L'utilisateur saisit un code sur le site officiel de Microsoft, validant ainsi lui-même l'accès de l'attaquant. **Note :** Cette méthode contourne les clés FIDO2 et les passkeys, car l'interaction avec le service Microsoft est authentique.
*   **Faiblesse opérationnelle :** Exposition de serveurs via des répertoires mal sécurisés et réutilisation de mots de passe (MySQL/Panels).

#### Recommandations pour les entreprises
*   **Restreindre le flux "Device Code" :** Désactiver cette option dans l'accès conditionnel (Conditional Access) partout où elle n'est pas strictement nécessaire (ex: limiter aux appareils partagés type salles de réunion).
*   **Renforcer l'accès conditionnel :**
    *   Appliquer des politiques basées sur la localisation IP.
    *   Utiliser l'évaluation continue de l'accès (**CAE**) pour invalider immédiatement les jetons suspects.
*   **Surveillance et Détection :** 
    *   Auditer les journaux de connexion Entra pour détecter des jetons provenant du client ID `d3590ed6-52b3-4102-aeff-aad2292ab01c` (Microsoft Office) corrélés à des adresses IP inhabituelles.
    *   Chasser la présence d'outils RMM non autorisés (ex: agents XEOX).
*   **Défense :** Pour l'aspect AiTM, privilégier des méthodes MFA résistantes au phishing (FIDO2) qui lient l'authentification à l'origine du domaine. Pour l'abus de code d'appareil, seule une politique de blocage rigoureuse via l'accès conditionnel est efficace.

---
[Source](https://thehackernews.com/2026/07/misconfigured-server-reveals-three.html){:target="_blank"}
