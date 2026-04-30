---
title: 'Popular WordPress redirect plugin hid dormant backdoor for years'
date: 2026-04-30
permalink: /posts/2026/04/30/popular-wordpress-redirect-plugin-hid-dormant-backdoor-for-years/
tags:
- veille-cyber
- bleepingcomp
---
### Backdoor critique dans le plugin WordPress « Quick Page/Post Redirect »

Plus de 70 000 sites WordPress ont été exposés à une porte dérobée persistante introduite via le plugin « Quick Page/Post Redirect ». Découverte par le chercheur Austin Ginder, cette compromission par chaîne d'approvisionnement a permis l'injection de code arbitraire et des opérations de « parasite SEO » à l'insu des administrateurs.

**Points clés :**
*   **Mécanisme d'attaque :** Les versions 5.2.1 et 5.2.2 (2020-2021) intégraient un système de mise à jour automatique détourné vers un domaine tiers (`anadnet[.]com`).
*   **Discrétion :** La porte dérobée était « passive » : elle ne s'activait que pour les visiteurs non connectés, évitant ainsi d'être détectée par les administrateurs du site.
*   **Objectif :** Utilisation des ressources des sites infectés pour manipuler le référencement naturel (SEO) au profit d'opérateurs tiers.
*   **État actuel :** Bien que le domaine malveillant ne résolve plus, le mécanisme de mise à jour frauduleux est toujours présent sur les installations non corrigées, laissant une porte ouverte à une exécution de code à distance.

**Vulnérabilités :**
*   **Injection de code arbitraire / Porte dérobée :** Présente dans les versions 5.2.1 et 5.2.2.
*   **CVE :** Aucune CVE n'est associée à cet incident à ce jour.

**Recommandations :**
*   **Désinstallation immédiate :** Supprimer le plugin des sites infectés.
*   **Nettoyage :** Remplacer le plugin par une version saine et officielle (version 5.2.4 ou ultérieure) dès que celle-ci sera à nouveau disponible sur le répertoire WordPress.org.
*   **Vigilance :** Surveiller les fichiers du site pour détecter toute modification anormale liée aux versions compromises.

---
[Source](https://www.bleepingcomputer.com/news/security/popular-wordpress-redirect-plugin-hid-dormant-backdoor-for-years/){:target="_blank"}
