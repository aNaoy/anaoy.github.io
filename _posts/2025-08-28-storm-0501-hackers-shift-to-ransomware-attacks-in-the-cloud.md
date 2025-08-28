---
title: 'Storm-0501 hackers shift to ransomware attacks in the cloud'
date: 2025-08-28
permalink: /posts/2025/08/28/storm-0501-hackers-shift-to-ransomware-attacks-in-the-cloud/
tags:
- veille-cyber
- bleepingcomp
---
**Évolution de Storm-0501 : La menace évolue vers le ransomware dans le cloud**

Le groupe de menaces Storm-0501, précédemment connu pour ses attaques de ransomware traditionnelles ciblant des appareils, a adapté ses méthodes. Il se concentre désormais sur le vol de données, la destruction des sauvegardes et le chiffrement basé sur le cloud pour extorquer ses victimes, sans avoir recours à des outils de chiffrement classiques.

**Points Clés :**

*   **Changement de Tactique :** Storm-0501 abandonne le chiffrement sur site au profit d'attaques purement basées sur le cloud.
*   **Exploitation des Fonctionnalités Cloud :** Les attaquants abusent des fonctionnalités natives des environnements cloud pour l'exfiltration de données et la destruction de sauvegardes.
*   **Objectif d'Extorsion :** L'objectif est d'appliquer une pression maximale sur les victimes en les privant de leurs données et de leurs moyens de récupération.
*   **Victimes Ciblé :** Les attaques impliquent la compromission de domaines Active Directory et de locataires Entra ID, souvent en exploitant des failles dans le déploiement de Microsoft Defender.
*   **Accès et Persistance :** Les attaquants utilisent des comptes de synchronisation de répertoire volés pour identifier les ressources et, une fois un compte Administrateur Global sans authentification multifacteur compromis, ils établissent une persistance via des domaines fédérés malveillants.

**Vulnérabilités Exploités (non spécifié avec CVE dans l'article) :**

*   Vulnérabilités dans le déploiement de Microsoft Defender.
*   Utilisation de comptes de synchronisation de répertoire (DSA) volés.
*   Compte Administrateur Global sans authentification multifacteur (MFA).
*   Abus de l'action `Microsoft.Authorization/elevateAccess/action` pour obtenir des rôles Propriétaire dans Azure.

**Recommandations :**

*   **Protection Active :** Mettre en œuvre les protections recommandées par Microsoft Defender XDR.
*   **Détection et Chasse :** Utiliser les requêtes de chasse fournies par Microsoft pour identifier les tactiques de ce groupe.
*   **Authentification Multifacteur (MFA) :** S'assurer que tous les comptes, en particulier ceux avec des privilèges élevés, disposent de l'authentification multifacteur activée.
*   **Gestion des Domaines Fédérés :** Examiner attentivement et sécuriser la configuration des domaines fédérés pour éviter l'usurpation d'identité et le contournement de la MFA.
*   **Sécurité du Cloud :** Renforcer la sécurité des environnements cloud, y compris la surveillance des accès aux services de stockage et la protection des coffres-forts de clés.

---
[Source](https://www.bleepingcomputer.com/news/security/storm-0501-hackers-shift-to-ransomware-attacks-in-the-cloud/){:target="_blank"}
