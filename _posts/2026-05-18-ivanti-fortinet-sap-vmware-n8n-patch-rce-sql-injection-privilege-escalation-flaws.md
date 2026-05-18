---
title: 'Ivanti, Fortinet, SAP, VMware, n8n Patch RCE, SQL Injection, Privilege Escalation Flaws'
date: 2026-05-18
permalink: /posts/2026/05/18/ivanti-fortinet-sap-vmware-n8n-patch-rce-sql-injection-privilege-escalation-flaws/
tags:
- veille-cyber
- hackernews
---
### Vague de correctifs critiques pour des infrastructures logicielles majeures

Plusieurs éditeurs de logiciels ont publié des mises à jour de sécurité urgentes pour corriger des vulnérabilités critiques permettant l'exécution de code à distance (RCE), des élévations de privilèges et des injections SQL.

#### Points clés par fournisseur

*   **Ivanti (Xtraction) :** Une faille de contrôle externe de nom de fichier permet à un attaquant authentifié de lire des fichiers sensibles et d'écrire du code HTML arbitraire.
*   **Fortinet :** Des vulnérabilités de contrôle d'accès et d'autorisation dans FortiAuthenticator et FortiSandbox permettent à des attaquants non authentifiés d'exécuter des commandes arbitraires.
*   **SAP :** Des failles majeures dans S/4HANA et SAP Commerce Cloud exposent les systèmes à l'injection SQL et à l'exécution de code côté serveur via une mauvaise configuration.
*   **VMware (Fusion) :** Une vulnérabilité de type "Time-of-check Time-of-use" (TOCTOU) permet à un utilisateur local non administratif d'élever ses privilèges au niveau root.
*   **n8n :** Une série de cinq failles critiques liées à la pollution de prototype et à l'injection de commandes permet une exécution de code à distance et une compromission totale du serveur.

#### Vulnérabilités identifiées

| Logiciel | CVE | Impact principal |
| :--- | :--- | :--- |
| Ivanti Xtraction | CVE-2026-8043 | Divulgation d'informations / Fichiers |
| FortiAuthenticator | CVE-2026-44277 | RCE (non authentifié) |
| FortiSandbox | CVE-2026-26083 | RCE (non authentifié) |
| SAP S/4HANA | CVE-2026-34260 | Injection SQL |
| SAP Commerce | CVE-2026-34263 | RCE / Injection de code |
| VMware Fusion | CVE-2026-41702 | Élévation de privilèges (Root) |
| n8n | CVE-2026-42231/42232/44791/44789/44790 | RCE / Compromission totale |

#### Recommandations

*   **Appliquer les correctifs immédiatement :** Il est impératif de mettre à jour les solutions logicielles vers les versions corrigées listées par les éditeurs (notamment les versions 2026.2 pour Ivanti, 8.0.3 pour FortiAuthenticator, et les versions récentes de n8n comme la 1.123.43).
*   **Auditer les configurations :** Pour les environnements SAP et n8n, vérifier la configuration des droits d'accès et s'assurer que les entrées utilisateurs sont correctement validées.
*   **Surveillance :** Une liste exhaustive d'autres éditeurs (dont Microsoft, Apple, Google, Cisco, etc.) a également publié des bulletins de sécurité ; il est fortement conseillé de consulter les portails PSIRT respectifs de chaque solution utilisée dans votre infrastructure pour vérifier les vulnérabilités liées aux produits non mentionnés en détail ici.

---
[Source](https://thehackernews.com/2026/05/ivanti-fortinet-sap-vmware-n8n-patch.html){:target="_blank"}
