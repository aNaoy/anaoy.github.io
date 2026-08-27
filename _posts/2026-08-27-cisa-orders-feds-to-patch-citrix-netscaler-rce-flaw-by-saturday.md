---
title: 'CISA orders feds to patch Citrix NetScaler RCE flaw by Saturday'
date: 2026-08-27
permalink: /posts/2026/08/27/cisa-orders-feds-to-patch-citrix-netscaler-rce-flaw-by-saturday/
tags:
- veille-cyber
- bleepingcomp
---
### Urgence de sécurité : Correctifs obligatoires pour Citrix NetScaler

La CISA a ordonné aux agences fédérales américaines de corriger d'urgence leurs appliances Citrix NetScaler avant le samedi 29 août, en raison d'une exploitation active de vulnérabilités critiques.

**Points clés**
*   La faille **CVE-2026-8452** est désormais classée dans le catalogue des vulnérabilités exploitées (KEV) de la CISA.
*   Initialement présentée par Citrix comme une simple vulnérabilité de déni de service (DoS), des chercheurs ont démontré qu'elle permet une exécution de code à distance (RCE) avec les privilèges root.
*   Des attaques de type "pray and spray" sont activement observées dans la nature, visant à déployer des web shells sur les serveurs vulnérables.
*   Plus de 23 000 instances NetScaler restent exposées sur Internet.

**Vulnérabilités identifiées**
*   **CVE-2026-8452** : Dépassement de mémoire critique (RCE/DoS) affectant NetScaler ADC et Gateway.
*   **CVE-2026-19490 & CVE-2026-19489** : Vulnérabilités supplémentaires pouvant entraîner des DoS ou des contournements d'authentification.

**Recommandations**
*   **Appliquer les correctifs immédiatement** : Toutes les instances de NetScaler ADC et Gateway doivent être mises à jour vers les versions corrigées fournies par Citrix.
*   **Audit de sécurité** : Vérifier la présence de web shells ou de comportements anormaux sur les serveurs, car la faille est exploitée activement.
*   **Réduction de la surface d'exposition** : Limiter l'accès aux interfaces de gestion et aux serveurs virtuels Gateway depuis l'Internet public autant que possible.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-hackers-now-exploiting-citrix-netscaler-rce-flaw-in-attacks/){:target="_blank"}
