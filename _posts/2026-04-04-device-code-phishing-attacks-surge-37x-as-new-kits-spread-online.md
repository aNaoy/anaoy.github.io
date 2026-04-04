---
title: 'Device code phishing attacks surge 37x as new kits spread online'
date: 2026-04-04
permalink: /posts/2026/04/04/device-code-phishing-attacks-surge-37x-as-new-kits-spread-online/
tags:
- veille-cyber
- bleepingcomp
---
### Explosion des attaques par hameçonnage via code d'appareil

Le piratage exploitant le flux d'autorisation OAuth 2.0 (Device Authorization Grant) a connu une augmentation spectaculaire de 37,5 fois cette année. Cette technique détourne un mécanisme conçu pour simplifier la connexion d'appareils sans clavier (IoT, TV connectées) afin de voler des jetons d'accès et de rafraîchissement, permettant ainsi aux attaquants de prendre le contrôle total de comptes Microsoft 365 ou Entra.

**Points clés :**
*   **Démocratisation via le PhaaS (Phishing-as-a-Service) :** L'émergence de kits de phishing prêts à l'emploi, comme *EvilTokens*, permet à des cybercriminels peu expérimentés de mener ces attaques à grande échelle.
*   **Diversification des kits :** Les chercheurs ont identifié au moins 11 kits actifs (dont VENOM, CLURE, LINKID, DOCUPOLL) utilisant des thématiques variées (DocuSign, Microsoft Teams, Adobe, RH) pour tromper les utilisateurs.
*   **Tactiques évoluées :** Ces kits intègrent des protections anti-bot, des API rotatives et utilisent des plateformes cloud légitimes pour héberger leur infrastructure malveillante.
*   **Vulnérabilités :** Il ne s'agit pas d'une faille logicielle spécifique (CVE), mais d'un **abus de conception du protocole OAuth 2.0** visant les flux d'autorisation par code.

**Recommandations :**
*   **Configuration restrictive :** Désactiver le flux d'autorisation par code d'appareil via des politiques d'accès conditionnel (Conditional Access Policies) lorsqu'il n'est pas strictement nécessaire.
*   **Surveillance proactive :** Auditer régulièrement les journaux de connexion pour détecter des événements d'authentification par code d'appareil anormaux.
*   **Analyse contextuelle :** Surveiller les adresses IP suspectes et les sessions inhabituelles associées à ce type de flux d'authentification.

---
[Source](https://www.bleepingcomputer.com/news/security/device-code-phishing-attacks-surge-37x-as-new-kits-spread-online/){:target="_blank"}
