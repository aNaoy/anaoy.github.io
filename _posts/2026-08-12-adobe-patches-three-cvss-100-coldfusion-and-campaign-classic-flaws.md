---
title: 'Adobe Patches Three CVSS 10.0 ColdFusion and Campaign Classic Flaws'
date: 2026-08-12
permalink: /posts/2026/08/12/adobe-patches-three-cvss-100-coldfusion-and-campaign-classic-flaws/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques : Adobe publie des correctifs pour ColdFusion, Commerce et Campaign Classic

Adobe a déployé des correctifs de sécurité urgents pour corriger plusieurs failles critiques affectant ses solutions ColdFusion, Commerce et Campaign Classic. Ces vulnérabilités, dont certaines atteignent un score CVSS de 10.0, exposent les systèmes à une exécution de code arbitraire et à une élévation de privilèges.

**Points clés :**
*   Les mises à jour pour ColdFusion et Campaign Classic sont classées en **Priorité 1** (risque élevé d'exploitation active).
*   Bien qu'aucune preuve d'exploitation active ne soit constatée, la dangerosité des failles impose une application rapide des correctifs.
*   Les instances de Campaign Classic hébergées par Adobe ont déjà été sécurisées ; l'action est uniquement requise pour les déploiements sur site (on-premise).

**Vulnérabilités majeures :**
*   **CVE-2026-48362 (Score 10.0) :** Injection de commande OS dans ColdFusion.
*   **CVE-2026-71398 (Score 10.0) :** Autorisation incorrecte dans Campaign Classic (exécution de code).
*   **CVE-2026-27302 (Score 10.0) :** Autorisation incorrecte dans Campaign Classic (exécution de code).
*   **CVE-2026-48273 (Score 9.9) :** Injection "eval" dans ColdFusion.
*   **CVE-2026-71384 (Score 9.6) :** Autorisation incorrecte dans ColdFusion (déni de service).
*   **CVE-2026-71362 (Score 9.1) :** Autorisation incorrecte dans Commerce (élévation de privilèges).
*   **CVE-2026-48381 (Score 9.0) :** Injection SQL dans Campaign Classic.

**Recommandations :**
*   Appliquer les correctifs dès que possible, idéalement dans les **72 heures**.
*   Pour ColdFusion, effectuer la mise à jour vers les versions **2025.0.12** ou **2023.0.23**.
*   Pour Campaign Classic, effectuer la mise à jour vers la version **ACC v7 7.4.4 build 9400**.

---
[Source](https://thehackernews.com/2026/08/adobe-patches-three-cvss-100-coldfusion.html){:target="_blank"}
