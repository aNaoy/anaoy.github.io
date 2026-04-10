---
title: 'New VENOM phishing attacks steal senior executives Microsoft logins'
date: 2026-04-10
permalink: /posts/2026/04/10/new-venom-phishing-attacks-steal-senior-executives-microsoft-logins/
tags:
- veille-cyber
- bleepingcomp
---
### Menace PhaaS "VENOM" : Cible privilégiée des cadres dirigeants

La plateforme de phishing-as-a-service (PhaaS) dénommée « VENOM » mène des attaques hautement sophistiquées visant les comptes Microsoft de dirigeants d'entreprises (CEOs, CFOs, VPs). Opérant discrètement depuis novembre dernier via des accès fermés, cette menace contourne les outils de sécurité traditionnels pour capturer les identifiants et les jetons de session.

**Points clés :**
*   **Techniques d'évasion :** Utilisation de codes QR en Unicode, de messages personnalisés avec des fils de discussion factices et insertion d'e-mails dans des fragments d'URL (Base64) pour masquer la cible aux outils de filtrage.
*   **Méthodes d'attaque :**
    *   **AiTM (Adversary-in-the-Middle) :** Interception en temps réel des flux de connexion et des codes MFA via un site proxy.
    *   **Device Code Phishing :** Manipulation de la victime pour autoriser l'accès à son compte depuis un appareil malveillant.
*   **Objectif :** Établissement d'un accès persistant sur le compte de la victime, souvent par l'enregistrement d'un nouvel appareil ou l'obtention de jetons d'authentification.

**Vulnérabilités :**
*   Le fonctionnement repose sur l'exploitation des flux d'authentification Microsoft (AiTM et Device Code). Aucune CVE spécifique n'est mentionnée, car il s'agit d'une exploitation légitime détournée du protocole d'authentification (abus de logique).

**Recommandations :**
*   **Renforcement de l'authentification :** Passer aux clés de sécurité matérielles conformes à la norme **FIDO2**, qui sont résistantes au phishing.
*   **Politiques d'accès :** Désactiver le flux de code d'appareil (device code flow) lorsque celui-ci n'est pas strictement nécessaire pour l'activité métier.
*   **Contrôle strict :** Mettre en œuvre des politiques d'accès conditionnel renforcées pour limiter les possibilités d'abus de jetons (token abuse).

---
[Source](https://www.bleepingcomputer.com/news/security/new-venom-phishing-attacks-steal-senior-executives-microsoft-logins/){:target="_blank"}
