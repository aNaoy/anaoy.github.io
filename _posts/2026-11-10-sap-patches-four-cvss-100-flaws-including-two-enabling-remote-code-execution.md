---
title: 'SAP Patches Four CVSS 10.0 Flaws, Including Two Enabling Remote Code Execution'
date: 2026-11-10
permalink: /posts/2026/11/10/sap-patches-four-cvss-100-flaws-including-two-enabling-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les infrastructures SAP

SAP a corrigé quatre vulnérabilités majeures, toutes notées 10.0 sur l'échelle CVSS, permettant à un attaquant non authentifié de compromettre totalement les systèmes affectés sans interaction utilisateur.

**Points clés :**
*   Les failles touchent le serveur d'applications **SAP NetWeaver** et le **SAP Web Dispatcher**.
*   Les vecteurs d'attaque incluent la corruption de mémoire via le trafic WebSocket, l'usurpation d'identité de serveur et le contournement d'authentification SAML.
*   Les systèmes utilisant des versions de noyau (kernel) obsolètes qui ne sont plus maintenues sont également vulnérables et nécessitent une mise à niveau impérative.

**Vulnérabilités identifiées :**

*   **CVE-2026-76964 (ICM) & CVE-2026-89126 (Web Dispatcher) :** Ces failles (nommées *ICM2SHELL*) découlent d'une gestion défectueuse des messages WebSocket, permettant une exécution de code à distance (RCE) via une corruption de mémoire.
*   **CVE-2026-89103 (SAP Gateway) :** Nommée *PROXYGATE*, cette vulnérabilité permet à un attaquant externe de se faire passer pour un serveur d'application légitime, facilitant des actions non autorisées.
*   **CVE-2026-120017 (SAML 2.0) :** Un défaut de vérification des signatures permet à un attaquant de se connecter en tant qu'utilisateur arbitraire (y compris administrateur) sur les systèmes utilisant le Single Sign-On SAML.

**Recommandations :**
1.  **Application des correctifs :** Déployer prioritairement les SAP Notes (3778530, 3778556, 3798345, 3849308) disponibles sur le portail *SAP for Me*.
2.  **Mise à niveau des noyaux :** Mettre à jour les noyaux (kernels) vers des versions supportées et patchées.
3.  **Durcissement de la configuration :**
    *   **Gateway :** Restreindre la liste `prxyinfo` et configurer le paramètre `gw/acl_mode_proxy` à `1`. Limiter les ports d'accès.
    *   **SAML :** Auditer les fournisseurs d'identité de confiance et vérifier les logs d'accès pour détecter des connexions suspectes.
    *   **WebSocket :** Désactiver le support WebSocket en dernier recours si le correctif ne peut être appliqué immédiatement, tout en tenant compte de l'impact sur les fonctionnalités Fiori et ABAP Push Channels.

---
[Source](https://thehackernews.com/2026/11/sap-patches-four-cvss-100-flaws.html){:target="_blank"}
