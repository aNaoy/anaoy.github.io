---
title: 'Hackers target Microsoft 365 accounts with 81 million login attempts'
date: 2026-07-01
permalink: /posts/2026/07/01/hackers-target-microsoft-365-accounts-with-81-million-login-attempts/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne massive de « password spraying » contre Microsoft 365

Une vaste campagne de *password spraying* a généré plus de 81 millions de tentatives de connexion sur des comptes Microsoft 365 entre le 12 et le 26 juin. Les attaquants ont exploité des identifiants compromis lors de fuites de données antérieures pour s'authentifier via l'interface en ligne de commande (CLI) d'Azure. Cette offensive a permis de compromettre 78 comptes répartis au sein de 64 organisations.

**Points clés :**
*   **Méthode d'attaque :** Utilisation du mécanisme OAuth « Resource Owner Password Credentials » (ROPC), qui permet de contourner les processus d'authentification interactive.
*   **Origine :** Le trafic provient d'une plage d'adresses IPv6 appartenant à LSHIY LLC (AS32167).
*   **Impact :** L'attaque exploite des politiques d'accès conditionnel mal configurées pour outrepasser l'authentification multifacteur (MFA).

**Vulnérabilités :**
Il ne s'agit pas d'une faille logicielle spécifique (CVE), mais de défauts de configuration des politiques d'accès conditionnel (CAP) :
*   MFA limitée à certaines applications seulement (au lieu de « Toutes les applications cloud »).
*   Application de la MFA restreinte à des groupes d'utilisateurs spécifiques.
*   Politiques de sécurité configurées uniquement en mode « rapport » (non appliquées).
*   Utilisation du mécanisme ROPC, intrinsèquement incompatible avec les flux d'authentification moderne comme la MFA ou le SSO.

**Recommandations :**
*   **Généraliser la MFA :** Appliquer les politiques d'authentification multifacteur à l'ensemble des applications cloud et pour tous les utilisateurs, sans exception.
*   **Désactiver ROPC :** Restreindre ou interdire l'utilisation de flux d'authentification obsolètes comme ROPC qui contournent les contrôles de sécurité modernes.
*   **Auditer les politiques d'accès :** Vérifier que les politiques d'accès conditionnel sont bien en mode « activé » et non en mode « rapport seul ».
*   **Surveillance :** Renforcer la surveillance des tentatives de connexion via l'interface Azure CLI et détecter les anomalies de trafic provenant de plages IP suspectes.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-microsoft-365-accounts-with-81-million-login-attempts/){:target="_blank"}
