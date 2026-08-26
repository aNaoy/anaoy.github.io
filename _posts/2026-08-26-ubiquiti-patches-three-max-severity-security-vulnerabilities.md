---
title: 'Ubiquiti patches three max severity security vulnerabilities'
date: 2026-08-26
permalink: /posts/2026/08/26/ubiquiti-patches-three-max-severity-security-vulnerabilities/
tags:
- veille-cyber
- bleepingcomp
---
### Ubiquiti : Correction de vulnérabilités critiques sur les systèmes UniFi

Ubiquiti a publié des correctifs pour trois vulnérabilités de sévérité maximale permettant à des attaquants distants non authentifiés de compromettre des appareils sans interaction utilisateur. Ces failles s'ajoutent à 18 autres vulnérabilités critiques corrigées récemment, soulignant la récurrence des cibles matérielles de la marque par des groupes malveillants, notamment pour la constitution de botnets.

**Points clés :**
*   **Risque élevé :** Les vulnérabilités sont exploitables à distance, sans privilèges et ne nécessitent aucune interaction de la part de l'utilisateur.
*   **Exposition importante :** Plus de 100 000 instances UniFi OS sont accessibles via Internet, constituant une surface d'attaque massive.
*   **Historique :** Les équipements Ubiquiti sont fréquemment utilisés par des acteurs étatiques pour mener des activités d'espionnage ou créer des réseaux de machines zombies.

**Vulnérabilités :**
*   **CVE-2026-77537 :** Mauvaise validation des entrées dans la plateforme UniFi Protect, permettant une compromission complète.
*   **CVE-2026-77550 :** Injection CRLF dans UniFi OS, permettant de contourner l'authentification.
*   **CVE-2026-77554 :** Injection de commande dans UniFi Talk, causée par une mauvaise validation des entrées.

**Recommandations :**
Il est impératif de mettre à jour les systèmes vers les versions suivantes (ou ultérieures) dès que possible :
*   **UniFi Protect Application :** version 7.2.105 ou supérieure.
*   **UniFi Talk Application :** version 5.3.2 ou supérieure.
*   **UniFi OS Server :** version 5.1.21 ou supérieure.

---
[Source](https://www.bleepingcomputer.com/news/security/ubiquiti-patches-three-max-severity-security-vulnerabilities/){:target="_blank"}
