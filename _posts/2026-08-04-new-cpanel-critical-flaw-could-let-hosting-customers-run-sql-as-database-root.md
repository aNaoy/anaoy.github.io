---
title: 'New cPanel Critical Flaw Could Let Hosting Customers Run SQL as Database Root'
date: 2026-08-04
permalink: /posts/2026/08/04/new-cpanel-critical-flaw-could-let-hosting-customers-run-sql-as-database-root/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans cPanel : Élévation de privilèges et failles d'interface

cPanel a publié une mise à jour corrective majeure adressant plusieurs vulnérabilités critiques affectant cPanel & WHM ainsi que WP Squared. La faille la plus préoccupante permet à un utilisateur authentifié d'exécuter des commandes SQL avec les privilèges root de la base de données, pouvant potentiellement mener à une compromission totale du système d'exploitation.

**Points clés :**
*   **CVE-2026-58048 :** Faille d'injection SQL liée au processus de renommage de bases de données, provoquant une exécution dans le contexte administratif (Score CVSS : 9.4).
*   **CVE-2026-58047 :** Vulnérabilité de "HTTP request smuggling" dans le démon `cpsrvd`, permettant potentiellement le vol d'identifiants (Score CVSS : 5.6).
*   **Failles Exim :** Des vulnérabilités liées aux fichiers `.forward` et au parcours de répertoires (directory traversal) permettent une élévation de privilèges locaux.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs via le gestionnaire de mise à jour de WHM ou via la commande `/usr/local/cpanel/scripts/upcp --force`.
*   **Builds corrigés :** Assurez-vous d'être au minimum sur les versions 11.110.0.137, 11.118.0.71, 11.126.0.78, 11.134.0.48, 11.136.0.32 ou 138.1.6 (pour WP Squared).
*   **Contournements temporaires :**
    *   Pour **CVE-2026-58048** : Révoquer temporairement l'accès à la fonctionnalité MySQL pour les utilisateurs cPanel.
    *   Pour **CVE-2026-58047** : Désactiver la réutilisation des connexions backend en configurant `cpsrvd_keepalives_disabled=1` dans `/var/cpanel/cpanel.config` et redémarrer `cpsrvd`.
*   **Vigilance :** Les avis de sécurité étant parfois contradictoires sur les versions corrigées, il est conseillé de vérifier spécifiquement le numéro de build installé sur le serveur.

---
[Source](https://thehackernews.com/2026/08/new-cpanel-critical-flaw-could-let.html){:target="_blank"}
