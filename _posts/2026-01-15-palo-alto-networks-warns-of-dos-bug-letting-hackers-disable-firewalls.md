---
title: 'Palo Alto Networks warns of DoS bug letting hackers disable firewalls'
date: 2026-01-15
permalink: /posts/2026/01/15/palo-alto-networks-warns-of-dos-bug-letting-hackers-disable-firewalls/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité DoS Critique sur les Pare-feux Palo Alto Networks**

Une faille de sécurité, identifiée sous la référence CVE-2026-0227, a été corrigée par Palo Alto Networks. Cette vulnérabilité critique permettait à des attaquants non authentifiés de provoquer un déni de service (DoS) sur les pare-feux de nouvelle génération (fonctionnant sous PAN-OS 10.1 ou supérieur) et sur les configurations Prisma Access, lorsque les fonctionnalités de passerelle ou de portail GlobalProtect sont activées.

**Points Clés:**

*   **Nature de la Vulnérabilité :** Déni de Service (DoS) permettant de désactiver les protections du pare-feu.
*   **Impact :** Les tentatives répétées de déclencher cette faille entraînent le pare-feu en mode maintenance.
*   **Portée :** Affecte les pare-feux de nouvelle génération Palo Alto Networks et Prisma Access, spécifiquement lorsque GlobalProtect est activé.
*   **Exploitation :** Au moment de la publication, aucune preuve d'exploitation active n'avait été découverte, mais les mises à jour ont été publiées par précaution.

**Vulnérabilité(s) :**

*   **CVE-2026-0227 :** Vulnérabilité de déni de service permettant à des attaquants non authentifiés de désactiver les pare-feux Palo Alto Networks.

**Recommandations :**

*   **Mise à Jour Immédiate :** Il est impératif de mettre à jour les systèmes affectés vers les versions de correctif recommandées par Palo Alto Networks. Le tableau détaillé des versions et des mises à jour suggérées est disponible dans le bulletin de sécurité de l'éditeur.
*   **Cloud NGFW :** Aucune action n'est nécessaire pour les déploiements Cloud NGFW.
*   **Prisma Access :** La majorité des instances Prisma Access ont déjà été mises à jour, les autres sont en cours de planification pour l'application des correctifs.

---
[Source](https://www.bleepingcomputer.com/news/security/palo-alto-networks-warns-of-dos-bug-letting-hackers-disable-firewalls/){:target="_blank"}
