---
title: 'ACF plugin bug gives hackers admin on 50,000 WordPress sites'
date: 2026-01-21
permalink: /posts/2026/01/21/acf-plugin-bug-gives-hackers-admin-on-50000-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Escalade de privilèges sur des sites WordPress via ACF Extended

Une vulnérabilité critique affectant le plugin ACF Extended pour WordPress permet à des attaquants non authentifiés d'obtenir des droits d'administrateur. Cette faille, identifiée sous le nom de CVE-2025-14533, est présente dans les versions 0.9.2.1 et antérieures du plugin, utilisé par environ 100 000 sites web.

L'exploitation repose sur l'abus de la fonctionnalité "Insert User / Update User" du plugin, qui ne restreint pas correctement les rôles lors de la création ou de la modification d'utilisateurs via un formulaire. Cela permet à un attaquant de définir arbitrairement le rôle de l'utilisateur, y compris "administrateur", indépendamment des paramètres du champ de rôle, causant ainsi une compromission totale du site.

Bien qu'aucun cas d'exploitation active de cette faille spécifique n'ait été détecté, une activité de reconnaissance à grande échelle de plugins WordPress vulnérables est observée, ciblant divers plugins, dont Post SMTP et LiteSpeed Cache.

**Points clés :**

*   **Vulnérabilité :** Escalade de privilèges permettant d'obtenir des droits d'administrateur.
*   **Plugin affecté :** Advanced Custom Fields: Extended (ACF Extended).
*   **Versions affectées :** 0.9.2.1 et antérieures.
*   **Impact :** Prise de contrôle complète du site WordPress.
*   **Conditions d'exploitation :** Nécessite l'utilisation d'un formulaire "Create User" ou "Update User" avec un champ de rôle.
*   **Découverte :** Andrea Bocchetti.
*   **Correction :** Publiée dans la version 0.9.2.2 d'ACF Extended.

**Vulnérabilités mentionnées :**

*   **CVE-2025-14533 :** ACF Extended plugin (versions 0.9.2.1 et antérieures).
*   **CVE-2025-11833 :** Post SMTP plugin.
*   **CVE-2024-28000 :** LiteSpeed Cache plugin.

**Recommandations :**

*   Mettre à jour immédiatement le plugin ACF Extended vers la version 0.9.2.2 ou une version ultérieure.
*   Appliquer les mises à jour de sécurité pour les autres plugins mentionnés, notamment Post SMTP et LiteSpeed Cache.
*   Surveiller l'activité de reconnaissance sur les sites WordPress.

---
[Source](https://www.bleepingcomputer.com/news/security/acf-plugin-bug-gives-hackers-admin-on-50-000-wordpress-sites/){:target="_blank"}
