---
title: 'SAP Patches CVSS 10.0 Kernel Flaw Enabling Unauthenticated Remote Code Execution'
date: 2026-09-09
permalink: /posts/2026/09/09/sap-patches-cvss-100-kernel-flaw-enabling-unauthenticated-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les systèmes SAP

SAP a publié des correctifs urgents pour plusieurs vulnérabilités majeures permettant l'exécution de code à distance (RCE) sans authentification. Ces failles compromettent la confidentialité, l'intégrité et la disponibilité des données critiques de l'entreprise.

**Points clés :**
* Les vulnérabilités affectent le cœur du système (kernel) SAP et divers composants réseau.
* Les contrôles d'accès et les politiques de mots de passe habituels sont inefficaces car les failles sont exploitables avant toute étape d'authentification.
* L'exploitation peut mener à une prise de contrôle totale du serveur, incluant l'accès aux bases de données, aux identifiants et aux fichiers système.

**Vulnérabilités majeures :**
* **CVE-2026-44756 (Score 10.0 - "OVERPASS") :** Corruption de mémoire dans le traitement du SAP Extended Passport (EPP) due à une validation manquante lors de la désérialisation. Permet l'exécution de commandes système avec les privilèges d'administrateur SAP.
* **CVE-2026-58240 (Score 9.8 - "S4GET") :** Défaut logique dans le serveur de messagerie SAP NetWeaver. Permet une exécution de code à distance sur les systèmes S/4HANA via le port de connexion standard des clients SAP GUI.
* **CVE-2026-76969 (Score 9.4) :** Divulgation d'identifiants dans les applications multi-tenant (SAP CAP), permettant la manipulation de données.
* **CVE-2026-66768 (Score 9.0) :** Contrôle d'accès inapproprié dans SAP GUI pour Java, autorisant l'exécution de commandes arbitraires.

**Recommandations :**
* **Appliquer les correctifs immédiatement :** Prioriser la mise à jour des systèmes exposés sur Internet avant les instances internes.
* **Inventorier les actifs :** Répertorier tous les systèmes SAP en production pour s'assurer qu'aucun serveur n'est oublié.
* **Renforcer la surveillance :** Mettre en place une visibilité accrue sur la couche applicative SAP pour détecter toute tentative d'exploitation pendant le déploiement des correctifs.
* **Réduire l'exposition :** Bien que le filtrage réseau classique ne soit pas une solution complète, il est recommandé de limiter autant que possible l'accès aux interfaces SAP critiques.

---
[Source](https://thehackernews.com/2026/09/sap-patches-cvss-100-kernel-flaw.html){:target="_blank"}
