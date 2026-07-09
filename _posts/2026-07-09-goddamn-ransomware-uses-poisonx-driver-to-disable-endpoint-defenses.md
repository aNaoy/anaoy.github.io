---
title: 'GodDamn Ransomware Uses PoisonX Driver to Disable Endpoint Defenses'
date: 2026-07-09
permalink: /posts/2026/07/09/goddamn-ransomware-uses-poisonx-driver-to-disable-endpoint-defenses/
tags:
- veille-cyber
- hackernews
---
### GodDamn : Une menace évolutive exploitant des pilotes signés

Le ransomware **GodDamn**, considéré comme une évolution des familles *Beast* et *Monster* (développées par l'acteur Hyadina), se distingue par l'utilisation de techniques sophistiquées d'évasion de défense et de mouvement latéral. Identifié pour la première fois en mai 2026, il cible les infrastructures d'entreprise en neutralisant les solutions de sécurité avant le chiffrement des données.

**Points clés :**
*   **Technique BYOVD (Bring Your Own Vulnerable Driver) :** Le groupe utilise le pilote noyau **PoisonX** (`g11.sys`), une menace rare car signée numériquement par Microsoft, pour désactiver les logiciels antivirus et EDR (Endpoint Detection and Response) au niveau du noyau.
*   **Mode opératoire :** Après un accès initial, les attaquants déploient des outils de collecte d'identifiants (NirSoft), installent AnyDesk pour un accès distant persistant, et utilisent PsExec pour se déplacer latéralement sur le réseau.
*   **Evasion :** Utilisation d'un outil en mode utilisateur masqué sous un nom de processus légitime ("symantec.exe") pour compléter l'action du pilote malveillant.

**Vulnérabilités :**
*   L'attaque repose sur l'abus de pilotes légitimement signés mais vulnérables ou malveillants, permettant de contourner les protections du noyau Windows (pas de CVE spécifique attribuée au pilote PoisonX dans l'article, mais le risque est inhérent à la politique de signature de Microsoft).

**Recommandations :**
*   **Gestion des pilotes :** Implémenter et appliquer activement les listes de blocage des pilotes vulnérables via la fonctionnalité « Microsoft Vulnerable Driver Blocklist » dans Windows Defender.
*   **Contrôle des accès :** Restreindre l'utilisation d'outils d'administration à distance (AnyDesk, PsExec, PowerShell) par des politiques de moindre privilège.
*   **Surveillance EDR :** Configurer les outils de sécurité pour détecter les tentatives de chargement de pilotes non signés ou suspects et surveiller les comportements anormaux des processus système (ex: renommage de processus de sécurité).
*   **Durcissement des privilèges :** Empêcher les utilisateurs standards d'installer des pilotes ou d'exécuter des scripts non autorisés.

---
[Source](https://thehackernews.com/2026/07/goddamn-ransomware-uses-poisonx-driver.html){:target="_blank"}
