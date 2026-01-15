---
title: 'Palo Alto Fixes GlobalProtect DoS Flaw That Can Crash Firewalls Without Login'
date: 2026-01-15
permalink: /posts/2026/01/15/palo-alto-fixes-globalprotect-dos-flaw-that-can-crash-firewalls-without-login/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité DoS critique dans GlobalProtect de Palo Alto Networks

Une faille de sécurité de haute gravité a été corrigée par Palo Alto Networks dans son logiciel GlobalProtect Gateway et Portal. Cette vulnérabilité, référencée sous le code **CVE-2026-0227** (score CVSS de 7.7), permet à un attaquant non authentifié de provoquer une condition de déni de service (DoS) sur les pare-feux. En déclenchant de manière répétée cette faille, le pare-feu peut entrer en mode de maintenance, le rendant indisponible. La cause identifiée est une mauvaise gestion des conditions exceptionnelles (CWE-754).

**Points clés :**

*   **Nature de la faille :** Déni de service (DoS) permettant de rendre les pare-feux indisponibles sans nécessiter d'authentification.
*   **Impact :** Mise en mode maintenance du pare-feu après des tentatives répétées.
*   **Condition :** Applicable aux configurations de PAN-OS NGFW ou Prisma Access avec une passerelle ou un portail GlobalProtect activés. Les pare-feux Cloud NGFW ne sont pas affectés.
*   **Exploitation :** Il existe une preuve de concept (PoC) pour cette vulnérabilité, bien qu'aucune exploitation active en conditions réelles n'ait été confirmée à ce jour.

**Vulnérabilités :**

*   **CVE-2026-0227** (score CVSS 7.7) : Déni de service via mauvaise gestion des conditions exceptionnelles (CWE-754).

**Versions affectées :**

*   PAN-OS 12.1 < 12.1.3-h3, < 12.1.4
*   PAN-OS 11.2 < 11.2.4-h15, < 11.2.7-h8, < 11.2.10-h2
*   PAN-OS 11.1 < 11.1.4-h27, < 11.1.6-h23, < 11.1.10-h9, < 11.1.13
*   PAN-OS 10.2 < 10.2.7-h32, < 10.2.10-h30, < 10.2.13-h18, < 10.2.16-h6, < 10.2.18-h1
*   PAN-OS 10.1 < 10.1.14-h20
*   Prisma Access 11.2 < 11.2.7-h8
*   Prisma Access 10.2 < 10.2.10-h29

**Recommandations :**

*   Il n'existe pas de mesures d'atténuation (workaround) pour cette faille.
*   La seule recommandation est de mettre à jour les versions affectées de PAN-OS et Prisma Access vers les versions corrigées fournies par Palo Alto Networks. Il est conseillé de maintenir les dispositifs à jour, particulièrement compte tenu de l'activité de balayage observée sur les passerelles GlobalProtect exposées.

---
[Source](https://thehackernews.com/2026/01/palo-alto-fixes-globalprotect-dos-flaw.html){:target="_blank"}
