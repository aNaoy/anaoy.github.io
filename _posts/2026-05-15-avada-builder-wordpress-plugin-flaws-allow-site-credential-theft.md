---
title: 'Avada Builder WordPress plugin flaws allow site credential theft'
date: 2026-05-15
permalink: /posts/2026/05/15/avada-builder-wordpress-plugin-flaws-allow-site-credential-theft/
tags:
- veille-cyber
- bleepingcomp
---
# Vulnérabilités critiques dans l'extension Avada Builder pour WordPress

L'extension Avada Builder, utilisée sur environ un million de sites WordPress, présente deux failles de sécurité majeures permettant l'exfiltration de données sensibles, voire une prise de contrôle totale du site.

### Points clés
*   **Gravité :** Les vulnérabilités permettent la lecture arbitraire de fichiers (dont `wp-config.php`) et l'injection SQL.
*   **Origine :** Découvertes par le chercheur Rafie Muhammad via le programme de bug bounty de Wordfence.
*   **Correctif :** La version 3.15.3, déployée le 12 mai, corrige l'intégralité des problèmes identifiés.

### Vulnérabilités identifiées
*   **CVE-2026-4782 (Lecture arbitraire de fichiers) :** Affecte les versions jusqu'à la 3.15.2. Nécessite un accès utilisateur (niveau abonné). Une validation insuffisante des paramètres dans la fonction de rendu des shortcodes permet de lire des fichiers critiques comme `wp-config.php`, exposant ainsi les identifiants de base de données.
*   **CVE-2026-4798 (Injection SQL aveugle) :** Affecte les versions jusqu'à la 3.15.1. Cette faille peut être exploitée sans authentification si WooCommerce a été activé puis désactivé sur le site. Elle permet d'extraire des données de la base de données, incluant les hashs de mots de passe, via le paramètre `product_order`.

### Recommandations
*   **Mise à jour immédiate :** Les administrateurs de sites utilisant Avada Builder doivent mettre à jour l'extension vers la **version 3.15.3** sans délai.
*   **Audit :** Pour les sites ayant désactivé WooCommerce, vérifier l'intégrité des données et surveiller toute activité inhabituelle dans les journaux d'accès.

---
[Source](https://www.bleepingcomputer.com/news/security/avada-builder-wordpress-plugin-flaws-allow-site-credential-theft/){:target="_blank"}
