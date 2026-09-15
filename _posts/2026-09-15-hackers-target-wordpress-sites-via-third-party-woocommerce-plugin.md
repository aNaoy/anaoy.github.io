---
title: 'Hackers target WordPress sites via third-party WooCommerce plugin'
date: 2026-09-15
permalink: /posts/2026/09/15/hackers-target-wordpress-sites-via-third-party-woocommerce-plugin/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation active de la faille critique dans WooCommerce Wholesale Lead Capture

Des attaquants exploitent activement une vulnérabilité critique permettant le téléchargement arbitraire de fichiers dans le plugin WordPress "WooCommerce Wholesale Lead Capture". Cette faille est utilisée pour injecter des webshells PHP, offrant aux pirates un contrôle total sur les sites compromis. Plus de 100 000 tentatives d'attaques ont déjà été bloquées.

**Points clés :**
*   **Vulnérabilité :** Téléchargement arbitraire de fichiers sans authentification via l'action AJAX `wwlc_file_upload_handler`.
*   **Mécanisme :** Le paramètre utilisateur `file_settings` permet de manipuler la liste des extensions autorisées pour inclure `.php`, contournant ainsi les restrictions de sécurité.
*   **Impact :** Exécution de code à distance (RCE) et compromission complète du site.
*   **CVE :** CVE-2026-27540.
*   **Versions affectées :** 2.0.3.1 et antérieures.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **2.0.3.2** ou supérieure.
*   **Audit de sécurité :** Rechercher des fichiers PHP suspects dans les répertoires d'upload et inspecter les journaux pour toute requête vers `admin-ajax.php` utilisant `wwlc_file_upload_handler`.
*   **Nettoyage :** Supprimer tout compte administrateur inconnu. En cas de compromission avérée, il est fortement conseillé de restaurer le site à partir d'une sauvegarde saine plutôt que de tenter une suppression manuelle des portes dérobées.
*   **Filtrage :** Bloquer les adresses IP identifiées comme malveillantes via un pare-feu applicatif (WAF).

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-wordpress-sites-via-third-party-woocommerce-plugin/){:target="_blank"}
