---
title: 'SQLi flaw in Elementor Ally plugin impacts 250k+ WordPress sites'
date: 2026-03-12
permalink: /posts/2026/03/12/sqli-flaw-in-elementor-ally-plugin-impacts-250k-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique par injection SQL dans l'extension Ally pour WordPress

Une faille critique d'injection SQL affecte l'extension d'accessibilité « Ally » développée par Elementor, exposant plus de 250 000 sites WordPress à un risque d'extraction de données non autorisé.

**Points clés :**
*   **Vulnérabilité :** Injection SQL (SQLi) non authentifiée.
*   **Origine :** Mauvaise gestion des paramètres URL dans la méthode `get_global_remediations()`, permettant l'injection de métacaractères SQL malgré l'utilisation de `esc_url_raw()`.
*   **Impact :** Un attaquant peut manipuler les requêtes SQL pour extraire des informations sensibles via des techniques d'injection aveugle basée sur le temps (*time-based blind SQLi*).
*   **Conditions d'exploitation :** Le site doit avoir le module « Remediation » actif et être connecté à un compte Elementor.
*   **Statut :** Plus de 60 % des sites équipés n'ont pas encore installé le correctif.

**Vulnérabilité identifiée :**
*   **CVE-2026-2313 :** Affecte toutes les versions d'Ally jusqu'à la 4.0.3 incluse.

**Recommandations :**
*   **Mise à jour immédiate :** Mettre à jour l'extension Ally vers la version **4.1.0** ou supérieure.
*   **Sécurisation du cœur :** Appliquer sans délai la mise à jour **WordPress 6.9.2**, qui corrige dix vulnérabilités critiques supplémentaires (XSS, contournement d'autorisation, SSRF).

---
[Source](https://www.bleepingcomputer.com/news/security/sqli-flaw-in-elementor-ally-plugin-impacts-250k-plus-wordpress-sites/){:target="_blank"}
