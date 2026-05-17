---
title: 'Tycoon2FA hijacks Microsoft 365 accounts via device-code phishing'
date: 2026-05-17
permalink: /posts/2026/05/17/tycoon2fa-hijacks-microsoft-365-accounts-via-device-code-phishing/
tags:
- veille-cyber
- bleepingcomp
---
### Résurgence de Tycoon2FA : détournement de comptes Microsoft 365 par phishing de code d'appareil

Malgré une opération policière internationale en mars, la plateforme de phishing Tycoon2FA est de nouveau opérationnelle. Elle utilise désormais le flux d'autorisation OAuth 2.0 (phishing par code d'appareil) pour compromettre les comptes Microsoft 365. Cette méthode contourne l'authentification multifacteur (MFA) en incitant la victime à autoriser un appareil contrôlé par l'attaquant.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation détournée des URL de suivi de clics de la plateforme de sécurité légitime *Trustifi*.
*   **Mécanisme :** La victime est redirigée vers une fausse page Microsoft. Elle est incitée à copier un code d'appareil sur la page officielle `microsoft.com/devicelogin`. Une fois le code validé, les attaquants reçoivent des jetons d'accès OAuth, leur offrant un accès illimité aux données (e-mails, fichiers, calendrier).
*   **Résilience :** Le kit intègre des techniques avancées d'obfuscation et de détection pour bloquer les outils d'analyse, les bacs à sable (sandboxes) et les bots de sécurité (plus de 230 noms de fournisseurs bloqués).

**Vulnérabilités :**
*   Le détournement repose sur l'abus du flux d'autorisation **OAuth 2.0 Device Authorization Grant**. (Note : il s'agit d'une vulnérabilité logique liée à l'ingénierie sociale plutôt qu'à une CVE spécifique).

**Recommandations de sécurité :**
*   **Configuration :** Désactiver le flux de code d'appareil OAuth s'il n'est pas strictement nécessaire.
*   **Gestion des accès :** Restreindre les permissions de consentement OAuth, exiger l'approbation de l'administrateur pour les applications tierces et appliquer des politiques d'accès aux appareils conformes.
*   **Surveillance :** Activer l'Évaluation continue de l'accès (CAE) et monitorer étroitement les journaux Entra (Entra logs) à la recherche d'authentifications par `deviceCode`, d'utilisations du *Microsoft Authentication Broker* ou de signatures suspectes de type *Node.js*.
*   **Protection :** Utiliser les indicateurs de compromission (IoCs) fournis par les chercheurs pour mettre à jour les règles de détection.

---
[Source](https://www.bleepingcomputer.com/news/security/tycoon2fa-hijacks-microsoft-365-accounts-via-device-code-phishing/){:target="_blank"}
