---
title: 'Regular Password Resets Aren’t as Safe as You Think'
date: 2026-04-23
permalink: /posts/2026/04/23/regular-password-resets-arent-as-safe-as-you-think/
tags:
- veille-cyber
- bleepingcomp
---
### La vulnérabilité du processus de réinitialisation des mots de passe

La réinitialisation des mots de passe représente une faille de sécurité majeure, souvent exploitée par des groupes cybercriminels (comme *Scattered Spider*) pour contourner l'authentification multifacteur (MFA). Par le biais d'ingénierie sociale, les attaquants usurpent l'identité d'un employé auprès du service desk pour obtenir de nouveaux identifiants, leur permettant ensuite d'accéder à l'Active Directory, d'extraire des bases de données de hachage (NTDS.dit) et de se déplacer latéralement pour déployer des ransomwares.

**Points clés :**
*   **Risque lié à l'humain :** Le service desk est une cible privilégiée car les agents ne disposent souvent pas de moyens fiables pour vérifier l'identité réelle de l'appelant.
*   **Coût élevé :** Chaque réinitialisation manuelle génère des coûts opérationnels significatifs (estimés à 70 $).
*   **Impact métier :** Une usurpation réussie peut mener à des compromissions totales, entraînant des pertes financières massives (ex: affaire Marks & Spencer en 2025).

**Vulnérabilités :**
*   **Ingénierie sociale :** Manipulation des processus de vérification manuelle du support informatique.
*   **Faiblesse des processus de secours :** Transmission de mots de passe temporaires via des canaux non sécurisés (email, voix).

**Recommandations :**
1.  **Privilégier le libre-service (SSPR) :** Réduire la dépendance envers le service desk en encourageant l'adoption d'outils de réinitialisation autonomes sécurisés.
2.  **Automatiser la vérification d'identité :** Implémenter des solutions qui exigent une authentification forte (code à usage unique vers un appareil de confiance ou via des fournisseurs d'identité comme Okta/Duo) avant toute action.
3.  **Sécuriser les identifiants temporaires :** Utiliser des mots de passe uniques et éphémères, transmis via des canaux chiffrés.
4.  **Surveillance active :** Auditer les journaux d'activité pour identifier les comportements suspects (fréquence anormale de demandes) et standardiser strictement les procédures de vérification pour éviter la subjectivité des agents.

---
[Source](https://www.bleepingcomputer.com/news/security/regular-password-resets-arent-as-safe-as-you-think/){:target="_blank"}
