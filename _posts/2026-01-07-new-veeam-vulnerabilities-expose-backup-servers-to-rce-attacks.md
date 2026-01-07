---
title: 'New Veeam vulnerabilities expose backup servers to RCE attacks'
date: 2026-01-07
permalink: /posts/2026/01/07/new-veeam-vulnerabilities-expose-backup-servers-to-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Veeam : Vulnérabilités Critiques Exposant les Serveurs de Sauvegarde**

Plusieurs failles de sécurité ont été corrigées dans le logiciel Veeam Backup & Replication, dont une vulnérabilité critique permettant l'exécution de code à distance (RCE).

**Points Clés :**

*   Le logiciel Veeam Backup & Replication est une solution d'entreprise pour la sauvegarde et la restauration de données critiques.
*   Il est fréquemment ciblé par des groupes de ransomwares cherchant à pivoter vers d'autres systèmes ou à empêcher la restauration des données.
*   Des groupes comme Cuba, FIN7, Frag, Akira et Fog ont déjà exploité des vulnérabilités Veeam dans des attaques.

**Vulnérabilités :**

*   **CVE-2025-59470 :** Vulnérabilité RCE critique permettant l'exécution de code à distance en tant qu'utilisateur `postgres` via un paramètre d'intervalle ou de commande malveillant. Elle affecte Veeam Backup & Replication 13.0.1.180 et les versions antérieures de la branche 13. Bien que critique, son exploitation nécessite les rôles "Backup Operator" ou "Tape Operator".
*   **CVE-2025-55125 :** Vulnérabilité de haute sévérité permettant l'exécution de code à distance à des opérateurs de sauvegarde ou de bande malveillants via la création d'un fichier de configuration de sauvegarde malveillant.
*   **CVE-2025-59468 :** Vulnérabilité de sévérité moyenne permettant l'exécution de code à distance à des opérateurs de sauvegarde ou de bande malveillants via l'envoi d'un paramètre de mot de passe malveillant.
*   **CVE-2024-40711 :** Une autre vulnérabilité RCE critique déjà exploitée par des ransomwares tels que Frag, Akira et Fog.

**Recommandations :**

*   Appliquer les mises à jour de sécurité publiées par Veeam pour corriger ces vulnérabilités. La version 13.0.1.1071 corrige CVE-2025-59470, CVE-2025-55125 et CVE-2025-59468.
*   Suivre les directives de sécurité recommandées par Veeam pour renforcer la protection des rôles "Backup Operator" et "Tape Operator", considérés comme hautement privilégiés.

---
[Source](https://www.bleepingcomputer.com/news/security/new-veeam-vulnerabilities-expose-backup-servers-to-rce-attacks/){:target="_blank"}
