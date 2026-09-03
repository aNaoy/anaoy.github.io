---
title: 'WordPress backup plugin flaw exposes millions of sites to takeover attacks'
date: 2026-09-03
permalink: /posts/2026/09/03/wordpress-backup-plugin-flaw-exposes-millions-of-sites-to-takeover-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans l'extension WordPress « All-in-One WP Migration »

Une faille de sécurité majeure affecte l'extension « All-in-One WP Migration and Backup », largement utilisée pour la gestion et le transfert de sites WordPress. Bien qu'un correctif soit disponible, plus de 3,25 millions de sites demeurent vulnérables à des attaques de prise de contrôle total.

**Points clés :**
*   **Mécanisme d'attaque :** La faille repose sur une injection SQL de second ordre. Un attaquant peut injecter du code malveillant via les "trackbacks" WordPress, qui s'exécute lorsque l'administrateur du site effectue une opération de sauvegarde ou de restauration.
*   **Conséquences :** L'exploitation permet de récupérer la clé secrète d'importation (`ai1wm_secret_key`), ouvrant la voie à l'injection d'archives malveillantes contenant du code exécutable distant.
*   **Ampleur :** Plus de 5 millions d'installations actives sont concernées, avec une majorité d'utilisateurs n'ayant pas encore appliqué la mise à jour corrective.

**Vulnérabilité :**
*   **CVE-2026-19949 :** Injection SQL de second ordre (versions 7.109 et antérieures).

**Recommandations :**
*   **Mise à jour immédiate :** Mettre à jour l'extension vers la **version 7.110 ou supérieure**, dans laquelle ServMask a corrigé la faille.
*   **Vigilance :** Même si l'extension est désactivée, elle reste une menace potentielle si elle est réactivée temporairement ; assurez-vous qu'elle soit supprimée ou maintenue à jour en permanence.

---
[Source](https://www.bleepingcomputer.com/news/security/wordpress-backup-plugin-flaw-exposes-millions-of-sites-to-takeover-attacks/){:target="_blank"}
