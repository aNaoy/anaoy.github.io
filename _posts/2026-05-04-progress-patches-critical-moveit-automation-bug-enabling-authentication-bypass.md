---
title: 'Progress Patches Critical MOVEit Automation Bug Enabling Authentication Bypass'
date: 2026-05-04
permalink: /posts/2026/05/04/progress-patches-critical-moveit-automation-bug-enabling-authentication-bypass/
tags:
- veille-cyber
- hackernews
---
### Sécurisation critique de MOVEit Automation : Correctifs pour des failles d'authentification

Progress Software a publié des mises à jour correctives pour MOVEit Automation afin de remédier à deux vulnérabilités majeures au niveau de l'interface des ports de commande du backend. Ces failles pourraient permettre à un attaquant non authentifié d'obtenir un accès administratif et de compromettre la confidentialité des données.

**Points clés :**
*   Les vulnérabilités touchent plusieurs versions de la solution de transfert de fichiers géré (MFT) MOVEit Automation.
*   Aucune solution de contournement n'est disponible ; la mise à jour logicielle est la seule mesure efficace.
*   Bien qu'aucune exploitation active ne soit rapportée, l'historique des attaques par ransomwares sur les produits MOVEit impose une vigilance maximale.

**Vulnérabilités :**
*   **CVE-2026-4670 (Score CVSS 9.8) :** Vulnérabilité critique permettant de contourner l'authentification.
*   **CVE-2026-5174 (Score CVSS 7.7) :** Vulnérabilité liée à une validation incorrecte des entrées, pouvant mener à une élévation de privilèges.

**Recommandations :**
Il est impératif de mettre à jour immédiatement MOVEit Automation vers les versions corrigées suivantes :
*   **Version 2025.1.5** (pour les versions <= 2025.1.4)
*   **Version 2025.0.9** (pour les versions <= 2025.0.8)
*   **Version 2024.1.8** (pour les versions <= 2024.1.7)

---
[Source](https://thehackernews.com/2026/05/progress-patches-critical-moveit.html){:target="_blank"}
