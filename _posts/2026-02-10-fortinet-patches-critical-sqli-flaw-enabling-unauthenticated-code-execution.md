---
title: 'Fortinet Patches Critical SQLi Flaw Enabling Unauthenticated Code Execution'
date: 2026-02-10
permalink: /posts/2026/02/10/fortinet-patches-critical-sqli-flaw-enabling-unauthenticated-code-execution/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilité Critique chez Fortinet Permettant l'Exécution de Code**

Une faille de sécurité critique a été corrigée par Fortinet dans son logiciel FortiClientEMS. Cette vulnérabilité, identifiée sous le code CVE-2026-21643, a une note de sévérité de 9.1 sur 10. Elle permet à un attaquant non authentifié d'exécuter du code arbitraire à distance en exploitant des requêtes HTTP spécialement conçues. Cette faille est de type "injection SQL" (CWE-89).

**Versions Affectées :**

*   FortiClientEMS 7.4.4 (nécessite une mise à niveau vers la version 7.4.5 ou supérieure)

Les versions 7.2 et 8.0 ne sont pas affectées par cette vulnérabilité spécifique.

**Recommandations :**

*   Mettre à jour FortiClientEMS vers la version 7.4.5 ou une version ultérieure pour les systèmes utilisant la branche 7.4.
*   Appliquer rapidement les correctifs de sécurité fournis par Fortinet.

Il est à noter que Fortinet mentionne également avoir récemment corrigé une autre faille critique (CVE-2026-24858) affectant plusieurs de ses produits (FortiOS, FortiManager, FortiAnalyzer, FortiProxy, FortiWeb). Cette dernière permettait à des attaquants de prendre le contrôle d'autres appareils via une fonctionnalité d'authentification SSO FortiCloud mal configurée, et il a été confirmé que cette vulnérabilité faisait l'objet d'exploitations actives par des acteurs malveillants pour établir une persistance, modifier des configurations et exfiltrer des données.

---
[Source](https://thehackernews.com/2026/02/fortinet-patches-critical-sqli-flaw.html){:target="_blank"}
