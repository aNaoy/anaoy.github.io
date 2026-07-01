---
title: 'Azure CLI Password Spray Hits at Least 78 Microsoft Accounts in 81M+ Attempts'
date: 2026-07-01
permalink: /posts/2026/07/01/azure-cli-password-spray-hits-at-least-78-microsoft-accounts-in-81m-attempts/
tags:
- veille-cyber
- hackernews
---
### Attaque massive par "Password Spray" contre l'interface Azure CLI

Une campagne automatisée de "password spray" cible l'interface de ligne de commande (CLI) d'Azure, exploitant des combinaisons d'identifiants fuités pour compromettre des comptes Microsoft. Entre le 12 et le 26 juin, plus de 81 millions de tentatives ont été enregistrées, aboutissant à la compromission d'au moins 78 comptes répartis dans 64 organisations.

**Points clés :**
*   **Origine :** L'attaque provient principalement d'une plage d'adresses IPv6 (2a0a:d683::/32) associée à l'infrastructure LSHIY LLC (AS32167).
*   **Technique de contournement :** Les attaquants exploitent le flux obsolète **ROPC** (*Resource Owner Password Credentials*). Ce protocole OAuth 2.0 legacy permet aux applications de manipuler directement les identifiants, ce qui court-circuite souvent les politiques d'accès conditionnel (CAP) et les mécanismes d'authentification multifacteur (MFA).
*   **Vulnérabilité :** Il ne s'agit pas d'une faille logicielle spécifique (CVE non applicable), mais d'une faiblesse de configuration des politiques de sécurité (CAP) qui ne couvrent pas l'intégralité des applications cloud, des utilisateurs ou des types de clients.

**Recommandations :**
*   **Généralisation du MFA :** Appliquer les politiques MFA à "Tous les utilisateurs", "Toutes les applications cloud" et "Tous les types d'applications clientes".
*   **Désactivation des flux legacy :** Restreindre ou supprimer l'utilisation des flux OAuth obsolètes comme le ROPC, qui ne sont pas compatibles avec les méthodes d'authentification modernes.
*   **Durcissement des accès :** Restreindre l'utilisation de l'application Azure CLI aux seuls utilisateurs ayant des besoins administratifs justifiés.
*   **Audit de configuration :** Vérifier que les politiques d'accès conditionnel ne contiennent pas d'exceptions basées sur des groupes restreints ou des localisations, permettant ainsi aux attaquants de s'infiltrer via des protocoles moins sécurisés.

---
[Source](https://thehackernews.com/2026/07/azure-cli-password-spray-hits-at-least.html){:target="_blank"}
