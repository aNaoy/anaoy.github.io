---
title: 'Cl0p Affiliates Target Internet-Exposed PTC Windchill and FlexPLM with Unauthenticated RCE'
date: 2026-07-25
permalink: /posts/2026/07/25/cl0p-affiliates-target-internet-exposed-ptc-windchill-and-flexplm-with-unauthenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Campagne d'extorsion Cl0p ciblant PTC Windchill et FlexPLM

Des attaquants affiliés au groupe de ransomware Cl0p exploitent activement des vulnérabilités critiques dans les solutions PTC Windchill et FlexPLM exposées sur Internet. Cette campagne vise principalement les secteurs de l'industrie, de l'automobile, de l'aérospatiale et de la vente au détail pour mener des opérations de double extorsion.

**Points clés :**
*   **Mode opératoire :** Les attaquants enchaînent deux vulnérabilités pour obtenir une exécution de code à distance (RCE) sans authentification.
*   **Objectif :** Déploiement de shells web JSP, énumération du système de fichiers, exfiltration de données de conception sensibles et extorsion financière.
*   **Modus operandi :** Utilisation de comptes compromis pour envoyer des demandes de rançon à grande échelle au sein des entreprises ciblées.

**Vulnérabilités exploitées :**
*   **CVE-2026-12569 (Score CVSS : 9.3) :** Flaille critique dans PTC Windchill permettant l'exécution de code à distance. Cette vulnérabilité est répertoriée dans le catalogue KEV (Known Exploited Vulnerabilities) de la CISA.
*   **Non nommée (Score CVSS : 7.5) :** Défaut de divulgation d'informations avant authentification dans le point de terminaison WSDL de FlexPLM, utilisé comme vecteur d'accès initial.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement les correctifs de sécurité fournis par PTC pour les systèmes Windchill et FlexPLM.
*   **Réduction de la surface d'attaque :** Limiter l'exposition des interfaces PTC Windchill et FlexPLM sur Internet.
*   **Surveillance :** Inspecter les serveurs à la recherche de fichiers JSP suspects dans le répertoire `/Windchill/login/`.
*   **Détection :** Surveiller les communications réseau et bloquer les adresses IP identifiées comme malveillantes : `216.152.148.54`, `216.152.151.204`, `104.243.35.63` et `5.180.41.35`.

---
[Source](https://thehackernews.com/2026/07/cl0p-affiliates-target-internet-exposed.html){:target="_blank"}
