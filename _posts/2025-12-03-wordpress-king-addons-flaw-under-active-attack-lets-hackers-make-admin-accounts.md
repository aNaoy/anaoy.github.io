---
title: 'WordPress King Addons Flaw Under Active Attack Lets Hackers Make Admin Accounts'
date: 2025-12-03
permalink: /posts/2025/12/03/wordpress-king-addons-flaw-under-active-attack-lets-hackers-make-admin-accounts/
tags:
- veille-cyber
- hackernews
---
**Exploitation Active d'une Faille Critique dans King Addons pour Elementor**

Une vulnérabilité de sécurité majeure affectant le plugin WordPress King Addons pour Elementor est activement exploitée. Cette faille, identifiée sous la référence CVE-2025-8489, permet à des attaquants non authentifiés d'obtenir des privilèges d'administrateur sur un site web.

**Points Clés :**

*   **Nature de la faille :** Escalade de privilèges.
*   **Impact :** Les attaquants peuvent s'attribuer le rôle d'administrateur lors de l'enregistrement d'un nouvel utilisateur.
*   **Fonctionnalité affectée :** La fonction `handle_register_ajax()` lors de l'enregistrement d'utilisateurs via le point de terminaison `/wp-admin/admin-ajax.php`.
*   **Exploitation :** Les attaques ont débuté fin octobre 2025, avec une exploitation massive constatée à partir du 9 novembre 2025. Plus de 48 400 tentatives d'exploitation ont été bloquées par Wordfence.

**Vulnérabilité :**

*   **CVE :** CVE-2025-8489
*   **Score CVSS :** 9.8
*   **Versions affectées :** 24.12.92 à 51.1.14
*   **Versions corrigées :** 51.1.35 (publiée le 25 septembre 2025)

**Recommandations :**

*   Mettre à jour le plugin King Addons pour Elementor vers la dernière version disponible (51.1.35 ou supérieure).
*   Auditer l'environnement pour détecter tout utilisateur administrateur suspect.
*   Surveiller les signes d'activité anormale sur le site web.

---
[Source](https://thehackernews.com/2025/12/wordpress-king-addons-flaw-under-active.html){:target="_blank"}
