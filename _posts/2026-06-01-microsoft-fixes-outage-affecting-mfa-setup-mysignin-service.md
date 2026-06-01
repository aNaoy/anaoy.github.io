---
title: 'Microsoft fixes outage affecting MFA setup, MySignIn service'
date: 2026-06-01
permalink: /posts/2026/06/01/microsoft-fixes-outage-affecting-mfa-setup-mysignin-service/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution de l'interruption du service My Sign-Ins de Microsoft

Une panne technique a récemment perturbé l'accès au portail *My Sign-Ins* de Microsoft et entravé la configuration de l'authentification multifacteur (MFA) pour de nombreux utilisateurs.

**Points clés :**
* **Nature de l'incident :** Les utilisateurs rencontraient des erreurs « 504 Gateway Timeout » lors de leurs tentatives d'accès aux services de gestion de sécurité.
* **Cause identifiée :** Une modification récente de la configuration du cache a nécessité un basculement vers une infrastructure alternative. Lors de cette opération, une surcharge de trafic (particulièrement en Europe) a provoqué un pic d'utilisation du processeur et de la mémoire, saturant la capacité de traitement du service.
* **Résolution :** Microsoft a annulé les changements de configuration et rétabli le trafic sur l'infrastructure d'origine pour restaurer un fonctionnement normal.

**Vulnérabilités :**
* Aucune CVE (Common Vulnerabilities and Exposures) n'est associée à cet incident, car il s'agit d'un problème de disponibilité et de performance lié à une configuration interne plutôt qu'à une faille de sécurité exploitable.

**Recommandations :**
* **Pour les administrateurs :** En cas d'indisponibilité des outils de gestion en ligne de Microsoft 365, consultez systématiquement le centre d'administration Microsoft (ou le compte *Microsoft 365 Status* sur X) pour vérifier si un incident global est en cours avant d'initier des procédures de dépannage locales.
* **Continuité de service :** Bien que l'infrastructure cloud soit hautement disponible, les organisations doivent maintenir des procédures de secours pour les processus critiques (comme la configuration MFA) lorsque des services dépendants de plateformes tierces subissent des interruptions techniques.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-outage-affecting-mfa-setup-mysignin-service/){:target="_blank"}
