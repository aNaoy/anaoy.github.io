---
title: 'Citrix urges admins to patch NetScaler flaws as soon as possible'
date: 2026-03-25
permalink: /posts/2026/03/25/citrix-urges-admins-to-patch-netscaler-flaws-as-soon-as-possible/
tags:
- veille-cyber
- bleepingcomp
---
### Urgence de mise à jour pour les infrastructures Citrix NetScaler

Citrix a publié des correctifs pour deux vulnérabilités critiques affectant les solutions NetScaler ADC et NetScaler Gateway. Ces failles présentent des risques importants, notamment pour les instances configurées en tant que fournisseurs d'identité (IdP) SAML ou serveurs d'accès distant.

**Points clés :**
*   **Vulnérabilité critique :** La faille **CVE-2026-3055** permet à un attaquant non authentifié de lire des données sensibles en mémoire (telles que des jetons de session) via un dépassement de mémoire (memory overread) dû à une validation insuffisante des entrées.
*   **Risque de confusion :** La faille **CVE-2026-4368** concerne les configurations Gateway (SSL VPN, ICA, RDP) et permet, via une condition de concurrence (race condition), de provoquer des erreurs de mélange de sessions utilisateurs.
*   **Historique préoccupant :** Des experts en cybersécurité soulignent la ressemblance technique entre la CVE-2026-3055 et les vulnérabilités "CitrixBleed", historiquement très exploitées par des acteurs malveillants.
*   **Exposition massive :** Plus de 30 000 instances NetScaler ADC et 2 300 Gateways sont actuellement exposées sur Internet.

**Vulnérabilités :**
*   **CVE-2026-3055 :** Fuite d'informations par lecture mémoire hors limites.
*   **CVE-2026-4368 :** Condition de concurrence (Race condition) impactant la gestion des sessions.

**Recommandations :**
*   **Application immédiate des correctifs :** Il est impératif de mettre à jour les versions vulnérables vers les versions corrigées :
    *   Versions 13.1 et 14.1 : Passer à la version **13.1-62.23** ou **14.1-66.59**.
    *   Versions 13.1-FIPS et 13.1-NDcPP : Passer à la version **13.1-37.262**.
*   **Surveillance :** Les administrateurs doivent consulter les directives officielles de Citrix pour identifier les instances vulnérables et surveiller toute activité anormale, en anticipant une ingénierie inverse des correctifs par les attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/citrix-urges-admins-to-patch-netscaler-flaws-as-soon-as-possible/){:target="_blank"}
