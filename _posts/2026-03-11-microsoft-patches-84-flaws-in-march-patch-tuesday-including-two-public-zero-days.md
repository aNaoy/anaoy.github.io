---
title: 'Microsoft Patches 84 Flaws in March Patch Tuesday, Including Two Public Zero-Days'
date: 2026-03-11
permalink: /posts/2026/03/11/microsoft-patches-84-flaws-in-march-patch-tuesday-including-two-public-zero-days/
tags:
- veille-cyber
- hackernews
---
### Microsoft Patch Tuesday : 84 vulnérabilités corrigées en mars 2026

Microsoft a publié des correctifs pour 84 vulnérabilités, dont huit sont classées comme critiques. Le rapport met en évidence une prédominance des failles d'élévation de privilèges (55 % des correctifs).

**Points clés :**
*   **Zero-days :** Deux vulnérabilités connues publiquement ont été corrigées.
*   **Répartition des failles :** 46 élévations de privilèges, 18 exécutions de code à distance (RCE), 10 divulgations d'informations, 4 dénis de service (DoS), 4 usurpations d'identité et 2 contournements de sécurité.
*   **Évolution :** Microsoft active désormais par défaut les "hotpatchs" pour Windows Autopatch afin d'accélérer le déploiement des correctifs sans nécessiter de redémarrage immédiat.

**Vulnérabilités majeures :**
*   **CVE-2026-21262 (Score 8.8) :** Élévation de privilèges dans SQL Server (Zero-day).
*   **CVE-2026-26127 (Score 7.5) :** Déni de service dans .NET (Zero-day).
*   **CVE-2026-21536 (Score 9.8) :** RCE critique dans le *Microsoft Devices Pricing Program* (déjà atténué).
*   **CVE-2026-25187 (Score 7.8) :** Élévation de privilèges dans Winlogon, permettant d'obtenir des droits SYSTEM sans interaction utilisateur.
*   **CVE-2026-26118 (Score 8.8) :** Server-Side Request Forgery (SSRF) dans Azure Model Context Protocol (MCP) permettant l'exfiltration de jetons d'identité.
*   **CVE-2026-26144 (Score 7.5) :** Divulgation d'informations critique dans Excel (Cross-site scripting) pouvant impacter Copilot Agent via une attaque "zero-click".

**Recommandations :**
*   Appliquer les correctifs de sécurité de mars 2026 sans délai sur l'ensemble du parc informatique.
*   Prioriser les correctifs pour les serveurs SQL et les systèmes exposant le protocole Azure MCP.
*   Surveiller les systèmes utilisant des outils d'IA et des agents Copilot pour détecter d'éventuelles extractions non autorisées de données.
*   Activer les mises à jour de sécurité de type "hotpatch" pour améliorer la réactivité face aux futures menaces.

---
[Source](https://thehackernews.com/2026/03/microsoft-patches-84-flaws-in-march.html){:target="_blank"}
