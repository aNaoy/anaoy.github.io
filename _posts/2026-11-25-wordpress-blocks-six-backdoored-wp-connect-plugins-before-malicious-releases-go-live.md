---
title: 'WordPress Blocks Six Backdoored WP Connect Plugins Before Malicious Releases Go Live'
date: 2026-11-25
permalink: /posts/2026/11/25/wordpress-blocks-six-backdoored-wp-connect-plugins-before-malicious-releases-go-live/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement : Six extensions WordPress piégées

L'équipe de sécurité de WordPress a bloqué six extensions développées par "WP Connect" après la découverte d'une porte dérobée (backdoor) insérée dans leurs mises à jour. L'attaque, résultant probablement du piratage du compte du développeur, visait à permettre une exécution de code à distance sur les sites utilisant ces outils.

**Points clés :**
*   **Action préventive :** WordPress a bloqué les versions malveillantes avant leur déploiement public grâce aux nouvelles protections automatisées de la plateforme.
*   **Mécanisme d'attaque :** Les extensions contenaient un module (`includes/airwp-online.php`) qui communiquait avec un serveur de commande et de contrôle (`tascredit-pay[.]com`) pour exécuter des commandes PHP arbitraires.
*   **Impact :** La vulnérabilité permettait le vol d'identifiants, la manipulation de fichiers, l'accès à la base de données et l'installation persistante de web shells.

**Vulnérabilité :**
*   **Référence :** CVE-2026-135202
*   **Sévérité :** Score CVSS de 9.8 (Critique)

**Extensions concernées :**
*   Air WP Sync (2.9.1 – 2.9.4)
*   WP Sync for Notion (1.7.4)
*   Add-on Brevo for Gravity Forms (2.6.3)
*   Add-On for Contact Form 7 to Airtable (2.5.4)
*   Add-On for Contact Form 7 to Notion (1.6.4)
*   Orders Sync to Airtable for WooCommerce (1.0.2)

**Recommandations :**
*   **Vérification :** Bien que les extensions n'aient pas été officiellement publiées, les administrateurs doivent vérifier leurs installations pour s'assurer qu'aucune version compromise n'est active.
*   **Suppression :** Désinstaller immédiatement toute instance des versions listées ci-dessus si elles sont présentes sur votre environnement.
*   **Audit :** En cas de doute, inspectez le répertoire `uploads` à la recherche de fichiers suspects et vérifiez les tâches planifiées (`WP-Cron`) pour détecter d'éventuels scripts persistants installés par les attaquants.

---
[Source](https://thehackernews.com/2026/11/wordpress-blocks-six-backdoored-wp.html){:target="_blank"}
