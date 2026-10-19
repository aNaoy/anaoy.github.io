---
title: 'Popular WordPress SEO Plugin Rank Math PRO Hijacked to Deliver Self-Restoring Backdoor'
date: 2026-10-19
permalink: /posts/2026/10/19/popular-wordpress-seo-plugin-rank-math-pro-hijacked-to-deliver-self-restoring-backdoor/
tags:
- veille-cyber
- hackernews
---
### Incident de cybersécurité : Backdoor persistante dans Rank Math PRO

Une version malveillante du plugin WordPress Rank Math PRO a été distribuée entre le 15 octobre (20:02 UTC) et le 16 octobre (07:12 UTC). Cette compromission de la chaîne d'approvisionnement injecte une porte dérobée (« backdoor ») persistante et auto-restauratrice sur les sites infectés.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-111862 (Score : 9.8/10).
*   **Impact :** Le malware crée des accès persistants (comptes administrateur, tâches planifiées, clés SSH) et peut se réinstaller automatiquement si les fichiers malveillants ne sont pas supprimés dans le bon ordre.
*   **Risque :** Compromission totale du site, vol de données, secrets (API, base de données) et accès serveur.
*   **Scope :** Uniquement la version PRO téléchargée ou mise à jour via le site `rankmath.com` durant la fenêtre critique. La version gratuite sur WordPress.org n'est pas concernée.

**Mesures de remédiation recommandées :**

1.  **Priorité absolue : Restauration de sauvegarde.** Si une sauvegarde saine antérieure au 15 octobre est disponible, restaurez-la et modifiez immédiatement l'intégralité des mots de passe et identifiants (Bases de données, WP-admin, FTP, SSH, clés API).
2.  **Nettoyage manuel (si aucune sauvegarde n'est disponible) :**
    *   Supprimer intégralement le répertoire du plugin `rank-math-pro`.
    *   Supprimer les entrées suivantes dans la table `wp_options` : `_uf6qdn2hmm`, `t8krdk990phb`, `_np5pvf754c`.
    *   Bloquer les connexions sortantes vers le domaine `rank1cdn.com`.
3.  **Audit post-nettoyage :**
    *   Rechercher des fichiers PHP suspects dans `mu-plugins`, les dossiers de thèmes et le répertoire `uploads`.
    *   Vérifier les comptes administrateurs suspects (ex: commençant par `wpsupport_` ou emails `@wp-mail.net`).
    *   Inspecter le fichier `wp-includes/class-wp-cache-util.php` (qui ne doit pas exister).
    *   Vérifier les configurations `.htaccess` et les tâches cron (`#ms6v46`).
4.  **Finalisation :**
    *   Installer la version propre (3.0.124) uniquement depuis l'espace client officiel de `rankmath.com`.
    *   Réinitialiser systématiquement toutes les clés de sécurité, mots de passe et accès distants.

---
[Source](https://thehackernews.com/2026/10/popular-wordpress-seo-plugin-rank-math.html){:target="_blank"}
