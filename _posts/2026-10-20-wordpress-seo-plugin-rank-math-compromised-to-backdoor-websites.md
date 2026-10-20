---
title: 'WordPress SEO plugin Rank Math compromised to backdoor websites'
date: 2026-10-20
permalink: /posts/2026/10/20/wordpress-seo-plugin-rank-math-compromised-to-backdoor-websites/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de l'extension WordPress Rank Math PRO : Attaque par chaîne d'approvisionnement

Une attaque par chaîne d'approvisionnement a ciblé l'extension WordPress **Rank Math PRO**. Entre le 15 octobre (20h02 UTC) et le 16 octobre (07h12 UTC), la version **3.0.123** distribuée sur le site officiel contenait un logiciel malveillant capable de compromettre les sites dès son activation. La version gratuite de l'extension n'est pas concernée.

**Points clés :**
*   **Nature de l'attaque :** Installation de portes dérobées persistantes et exfiltration de données sensibles.
*   **Fonctionnalités du malware :** Communication avec le domaine `rank1cdn[.]com`, création de comptes administrateurs factices (`wpsupport_`), exécution de commandes et vol d'identifiants (Cloud, AWS, SSH, bases de données, clés API).
*   **Indicateurs de compromission :** Présence du fichier malveillant `wp-includes/class-wp-cache-util.php`, entrée de base de données `_np5pvf754c` et tâche cron `#ms6v46`.

**Vulnérabilités :**
Aucune CVE spécifique n'a été assignée à cet incident, il s'agit d'une compromission directe des fichiers sources distribués par l'éditeur.

**Recommandations :**
*   **Mise à jour :** Si la version 3.0.123 a été installée, la mise à jour vers la version **3.0.124** (saine) est insuffisante pour supprimer le malware.
*   **Nettoyage manuel :** Supprimer intégralement le dossier de l'extension, supprimer les entrées malveillantes en base de données et traquer toute trace de persistance (nouveaux comptes admin, fichiers altérés, tâches planifiées).
*   **Restauration :** Privilégier une restauration complète depuis une sauvegarde saine antérieure au 15 octobre.
*   **Sécurisation post-incident :** Procéder au renouvellement immédiat de tous les secrets (mots de passe, clés API, clés SSH, *salts* de configuration).
*   **Filtrage :** Bloquer tout trafic sortant vers le domaine `rank1cdn[.]com` au niveau du pare-feu.

---
[Source](https://www.bleepingcomputer.com/news/security/wordpress-seo-plugin-rank-math-compromised-to-backdoor-websites/){:target="_blank"}
