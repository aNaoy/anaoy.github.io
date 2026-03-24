---
title: 'Citrix Urges Patching Critical NetScaler Flaw Allowing Unauthenticated Data Leaks'
date: 2026-03-24
permalink: /posts/2026/03/24/citrix-urges-patching-critical-netscaler-flaw-allowing-unauthenticated-data-leaks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Citrix NetScaler : Mesures de protection immédiates

Citrix a publié des correctifs pour deux vulnérabilités affectant les solutions NetScaler ADC et Gateway. Bien qu'aucune exploitation active ne soit rapportée pour le moment, la criticité des failles et l'historique des attaques sur ces produits imposent une mise à jour urgente.

**Vulnérabilités identifiées :**

*   **CVE-2026-3055 (Score CVSS 9.3) :** Lecture hors limites (out-of-bounds read) due à une validation insuffisante des entrées. Elle permet à un attaquant distant non authentifié de divulguer des informations sensibles en mémoire. Cette vulnérabilité ne concerne que les appliances configurées en tant que fournisseur d'identité SAML (SAML IdP).
*   **CVE-2026-4368 (Score CVSS 7.7) :** Problème de type "race condition" pouvant entraîner un mélange de sessions utilisateur. Cette faille affecte les dispositifs configurés comme passerelles (SSL VPN, ICA Proxy, etc.) ou serveurs d'authentification (AAA).

**Points clés :**
*   Les configurations par défaut ne sont pas nécessairement vulnérables ; l'exposition dépend de l'activation des rôles SAML IdP, Gateway ou AAA.
*   Les experts soulignent une similitude inquiétante avec les vulnérabilités "Citrix Bleed" précédentes, faisant craindre une exploitation rapide par des acteurs malveillants pour obtenir un accès initial aux réseaux d'entreprise.

**Recommandations :**
1.  **Vérification de la configuration :**
    *   Recherchez `add authentication samlIdPProfile .*` dans votre configuration pour identifier si l'appareil est un SAML IdP.
    *   Recherchez `add authentication vserver .*` ou `add vpn vserver .*` pour vérifier l'exposition au risque de mélange de sessions.
2.  **Application des correctifs :** Mettez à jour les instances vers les versions sécurisées dès que possible :
    *   **Versions 14.1 :** Mettre à jour vers 14.1-66.59 ou ultérieure.
    *   **Versions 13.1 :** Mettre à jour vers 13.1-62.23 ou ultérieure.
    *   **Versions FIPS/NDcPP 13.1 :** Mettre à jour vers 13.1-37.262 ou ultérieure.

---
[Source](https://thehackernews.com/2026/03/citrix-urges-patching-critical.html){:target="_blank"}
