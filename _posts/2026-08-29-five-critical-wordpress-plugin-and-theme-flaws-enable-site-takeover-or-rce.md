---
title: 'Five Critical WordPress Plugin and Theme Flaws Enable Site Takeover or RCE'
date: 2026-08-29
permalink: /posts/2026/08/29/five-critical-wordpress-plugin-and-theme-flaws-enable-site-takeover-or-rce/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les extensions et thèmes WordPress

Cinq vulnérabilités majeures ont été identifiées dans des extensions et thèmes WordPress populaires. Ces failles permettent aux attaquants de contourner l'authentification, d'escalader leurs privilèges, de prendre le contrôle total des sites ou d'exécuter du code arbitraire (RCE).

**Points clés :**
*   Les vulnérabilités touchent des outils largement utilisés comme WPMU DEV Dashboard, le thème Avada, TranslatePress, Pods et GiveWP.
*   La plupart des failles permettent une prise de contrôle totale par des attaquants non authentifiés.
*   Les causes racines incluent une mauvaise gestion de la sérialisation PHP, une confiance excessive dans les données provenant de la base de données et l'exposition de bibliothèques de développement en production.

**Vulnérabilités identifiées :**
*   **CVE-2026-76581 (WPMU DEV Dashboard) :** Contournement d'authentification via SSO permettant une prise de contrôle administrateur.
*   **CVE-2026-18431 (Thème Avada) :** Écriture arbitraire de fichiers conduisant à une exécution de code à distance (RCE).
*   **CVE-2026-19632 (TranslatePress) :** Exposition d'informations sensibles permettant de récupérer les URL de réinitialisation de mot de passe administrateur.
*   **CVE-2026-19598 (Pods) :** Élévation de privilèges permettant de modifier le mot de passe de n'importe quel utilisateur, y compris l'administrateur.
*   **CVE-2026-82222 (GiveWP) :** Injection d'objets PHP menant à une exécution de code à distance (RCE).

**Recommandations :**
*   Mettre à jour immédiatement les extensions et thèmes concernés vers leurs dernières versions corrigées.
*   Désactiver les fonctionnalités non nécessaires des plugins (comme le traitement automatique des chaînes dans TranslatePress ou les passerelles de paiement inutilisées).
*   Appliquer une politique de moindre privilège pour limiter l'impact en cas de compromission.
*   Surveiller les journaux d'activité pour détecter toute tentative d'accès non autorisé.

---
[Source](https://thehackernews.com/2026/08/five-critical-wordpress-plugin-and.html){:target="_blank"}
