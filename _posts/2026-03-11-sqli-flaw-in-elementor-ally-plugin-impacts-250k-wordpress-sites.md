---
title: 'SQLi flaw in Elementor Ally plugin impacts 250k+ WordPress sites'
date: 2026-03-11
permalink: /posts/2026/03/11/sqli-flaw-in-elementor-ally-plugin-impacts-250k-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique par injection SQL dans l'extension WordPress Ally

Une faille d'injection SQL critique menace plus de 250 000 sites WordPress utilisant l'extension d'accessibilité « Ally » d'Elementor. Cette vulnérabilité permet à des attaquants non authentifiés d'extraire des données sensibles de la base de données via des techniques d'injection SQL aveugle temporelle.

**Points clés :**
*   **Vulnérabilité :** Injection SQL (SQLi).
*   **CVE :** CVE-2026-2313.
*   **Cause technique :** Une mauvaise gestion des paramètres URL dans la méthode `get_global_remediations()`. L'utilisation de `esc_url_raw()` est insuffisante car elle ne bloque pas les métacaractères SQL, permettant leur concaténation directe dans une requête JOIN.
*   **Conditions d'exploitation :** Le plugin doit être connecté à un compte Elementor et le module « Remediation » doit être actif.
*   **Impact :** Plus de 250 000 sites restent vulnérables, seuls 36 % des utilisateurs ayant appliqué le correctif.

**Recommandations :**
*   **Mise à jour immédiate :** Mettre à jour l'extension Ally vers la version **4.1.0** ou supérieure.
*   **Maintenance système :** Installer sans délai la dernière mise à jour de WordPress (version 6.9.2), qui corrige dix vulnérabilités critiques supplémentaires (XSS, contournement d'autorisation et SSRF).

---
[Source](https://www.bleepingcomputer.com/news/security/sqli-flaw-in-elementor-ally-plugin-impacts-250k-plus-wordpress-sites/){:target="_blank"}
