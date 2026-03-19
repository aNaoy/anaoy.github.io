---
title: 'Max severity Ubiquiti UniFi flaw may allow account takeover'
date: 2026-03-19
permalink: /posts/2026/03/19/max-severity-ubiquiti-unifi-flaw-may-allow-account-takeover/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans l'application UniFi Network

Ubiquiti a publié des correctifs pour deux vulnérabilités majeures affectant l'application UniFi Network, utilisée pour la gestion des équipements réseau. Ces failles exposent les systèmes à des prises de contrôle de compte et à des escalades de privilèges.

**Points clés :**
*   L'application UniFi Network (UniFi Controller) est la cible fréquente d'acteurs malveillants cherchant à intégrer des équipements dans des botnets.
*   Les vulnérabilités permettent des attaques à faible complexité, ne nécessitant aucune interaction de l'utilisateur.

**Vulnérabilités identifiées :**
*   **CVE-2026-22557 (Sévérité maximale) :** Vulnérabilité de type "Path Traversal". Un attaquant ayant accès au réseau peut consulter des fichiers système sensibles, ce qui peut mener au détournement total de comptes utilisateur.
*   **Injection NoSQL authentifiée :** Permet à un attaquant disposant déjà d'un accès restreint au réseau d'élever ses privilèges au sein de l'application.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquez sans délai la version **10.1.89** ou une version ultérieure.
*   **Périmètre :** Cette mesure concerne tous les environnements où UniFi Network est déployé, qu'il s'agisse de serveurs dédiés, de postes de travail ou de passerelles cloud UniFi.

---
[Source](https://www.bleepingcomputer.com/news/security/ubiquiti-warns-of-unifi-flaw-that-may-enable-account-takeover/){:target="_blank"}
