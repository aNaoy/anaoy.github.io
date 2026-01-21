---
title: 'Zoom and GitLab Release Security Updates Fixing RCE, DoS, and 2FA Bypass Flaws'
date: 2026-01-21
permalink: /posts/2026/01/21/zoom-and-gitlab-release-security-updates-fixing-rce-dos-and-2fa-bypass-flaws/
tags:
- veille-cyber
- hackernews
---
Zoom et GitLab ont publié des mises à jour de sécurité pour corriger plusieurs failles critiques.

**Mises à jour Zoom**

*   **Vulnérabilité :** Injection de commandes dans les routeurs multimédias Zoom Node (MMR).
    *   **CVE :** CVE-2026-22844
    *   **Impact :** Permet à un participant à une réunion d'exécuter du code à distance sur le MMR via un accès réseau.
    *   **Score CVSS :** 9.9/10
    *   **Versions affectées :** Versions antérieures à 5.2.1716.0 pour Zoom Node Meetings Hybrid (ZMH) et Zoom Node Meeting Connector (MC).
    *   **Recommandation :** Mettre à jour les modules MMR vers la dernière version disponible.

**Mises à jour GitLab**

*   **Vulnérabilité :** Conditions de déni de service (DoS) et contournement de l'authentification à deux facteurs (2FA).
    *   **CVE-2025-13927 :** Permet à un utilisateur non authentifié de créer une condition de DoS en envoyant des requêtes malformées avec des données d'authentification corrompues.
        *   **Score CVSS :** 7.5
        *   **Versions affectées :** Toutes les versions à partir de 11.9 avant 18.6.4, 18.7 avant 18.7.2, et 18.8 avant 18.8.2.
    *   **CVE-2025-13928 :** Autorisation incorrecte dans l'API Releases, permettant à un utilisateur non authentifié de provoquer un DoS.
        *   **Score CVSS :** 7.5
        *   **Versions affectées :** Toutes les versions à partir de 17.7 avant 18.6.4, 18.7 avant 18.7.2, et 18.8 avant 18.8.2.
    *   **CVE-2026-0723 :** Permet de contourner le 2FA en soumettant des réponses d'appareil forgées, à condition de connaître l'identifiant des identifiants de la victime.
        *   **Score CVSS :** 7.4
        *   **Versions affectées :** Toutes les versions à partir de 18.6 avant 18.6.4, 18.7 avant 18.7.2, et 18.8 avant 18.8.2.
*   **Autres failles de sévérité moyenne :**
    *   CVE-2025-13335 (CVSS 6.5) : DoS via des documents Wiki malformés.
    *   CVE-2026-1102 (CVSS 5.3) : DoS via des requêtes d'authentification SSH malformées répétées.
*   **Recommandation :** Mettre à jour GitLab vers les versions corrigées.

---
[Source](https://thehackernews.com/2026/01/zoom-and-gitlab-release-security.html){:target="_blank"}
