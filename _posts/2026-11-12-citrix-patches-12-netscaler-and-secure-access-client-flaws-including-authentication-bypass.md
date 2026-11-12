---
title: 'Citrix Patches 12 NetScaler and Secure Access Client Flaws, Including Authentication Bypass'
date: 2026-11-12
permalink: /posts/2026/11/12/citrix-patches-12-netscaler-and-secure-access-client-flaws-including-authentication-bypass/
tags:
- veille-cyber
- hackernews
---
### Alert de Sécurité : Vulnérabilités Critiques dans les produits Citrix NetScaler

Citrix a publié des correctifs pour 12 vulnérabilités critiques affectant NetScaler ADC, Gateway, Console ainsi que les clients Secure Access. Ces failles exposent les systèmes à des risques de déni de service (DoS), de contournement d'authentification et d'élévation de privilèges.

**Points clés :**
*   **Nature des risques :** La majorité des vulnérabilités concernent des dépassements de mémoire (memory overflow) ou des corruptions de mémoire, pouvant entraîner un comportement erroné du système ou une interruption de service.
*   **Failles critiques :** Une vulnérabilité de contournement d'authentification dans NetScaler Console (CVE-2026-120869) permet à un attaquant non authentifié d'accéder à des ressources restreintes.
*   **Élévation de privilèges :** Des failles dans les clients Secure Access permettent à un utilisateur local de bas niveau d'obtenir les droits SYSTEM (Windows) ou ROOT (Linux).
*   **Contexte :** Ces correctifs font suite à une analyse approfondie du code via l'IA. Aucune exploitation active n'a été signalée à ce jour.

**Vulnérabilités majeures :**
*   **CVE-2026-120869 (Score 9.4) :** Contournement d'authentification (NetScaler Console).
*   **CVE-2026-107412 (Score 9.5) :** Multiples dépassements de mémoire (NetScaler Gateway/AAA).
*   **CVE-2026-120868, 107407-10, 107415, 111344, 120864 (Score 9.3) :** Diverses failles de dépassement/corruption mémoire (DoS).
*   **CVE-2026-118268 (Score 8.5) :** Élévation de privilèges (Secure Access Client Windows).
*   **CVE-2026-118269 (Score 8.5) :** Élévation de privilèges (Secure Access Client Linux).

**Recommandations :**
Il est impératif de mettre à jour immédiatement les infrastructures vers les versions corrigées :
*   **NetScaler ADC / Gateway :** Vers 14.1-73.57, 13.1-64.39 (ou versions ultérieures).
*   **NetScaler FIPS/NDcPP :** Vers 14.1-73.58 ou 13.1-37.293 (ou versions ultérieures).
*   **NetScaler Console :** Vers 14.1-74.34 ou plus.
*   **Secure Access Client :** Mise à jour vers 26.11.1.6 (Windows) et 26.10.4 (Linux).

---
[Source](https://thehackernews.com/2026/11/citrix-patches-12-netscaler-and-secure.html){:target="_blank"}
