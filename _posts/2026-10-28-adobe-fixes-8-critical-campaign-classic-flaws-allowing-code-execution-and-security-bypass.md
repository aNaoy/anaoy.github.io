---
title: 'Adobe Fixes 8 Critical Campaign Classic Flaws Allowing Code Execution and Security Bypass'
date: 2026-10-28
permalink: /posts/2026/10/28/adobe-fixes-8-critical-campaign-classic-flaws-allowing-code-execution-and-security-bypass/
tags:
- veille-cyber
- hackernews
---
### Correctifs critiques pour Adobe Campaign Classic et Connect

Adobe a publié des correctifs de sécurité traitant plusieurs vulnérabilités critiques dans **Adobe Campaign Classic** et **Adobe Connect**. Bien qu'aucune exploitation active ne soit signalée à ce jour, la sévérité des failles impose une mise à jour immédiate des systèmes concernés.

**Points clés :**
*   **Adobe Campaign Classic :** Huit vulnérabilités critiques affectant les versions 7.4.4 build 9402 et antérieures (Windows/Linux).
*   **Adobe Connect :** Une faille critique affectant les versions Desktop et Mobile.

**Vulnérabilités identifiées (Campaign Classic) :**
*   **Exécution de code arbitraire :** CVE-2026-104351, CVE-2026-104353, CVE-2026-105780 (Scores CVSS : 9.9).
*   **Contournement de sécurité (Injections SQL) :** CVE-2026-105489, CVE-2026-105781, CVE-2026-104354, CVE-2026-105779 (Scores CVSS : 9.1 à 9.9).
*   **Escalade de privilèges (XSS réfléchi) :** CVE-2026-104350 (Score CVSS : 9.3).

**Vulnérabilité identifiée (Adobe Connect) :**
*   **CVE-2026-48360 (Score CVSS : 9.6) :** Injection de code permettant l'exécution arbitraire sur Windows, macOS et Android.

**Recommandations :**
*   **Mise à jour Campaign Classic :** Installer la version **7.4.4 build 9403**.
*   **Mise à jour Adobe Connect Desktop :** Passer à la version **2026.9.61** (Windows), **2026.10.66** (macOS Silicon) ou **2026.10.170** (macOS Intel).
*   **Mise à jour Adobe Connect Mobile :** Passer à la version **4.5** pour Android.

---
[Source](https://thehackernews.com/2026/10/adobe-fixes-8-critical-campaign-classic.html){:target="_blank"}
