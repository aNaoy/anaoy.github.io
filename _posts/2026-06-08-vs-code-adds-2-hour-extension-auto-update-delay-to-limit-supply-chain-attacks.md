---
title: 'VS Code Adds 2-Hour Extension Auto-Update Delay to Limit Supply Chain Attacks'
date: 2026-06-08
permalink: /posts/2026/06/08/vs-code-adds-2-hour-extension-auto-update-delay-to-limit-supply-chain-attacks/
tags:
- veille-cyber
- hackernews
---
### Sécurisation des extensions VS Code : introduction d'un délai de mise à jour

Microsoft renforce la sécurité de Visual Studio Code (version 1.123+) en instaurant un délai automatique de deux heures avant l'installation des mises à jour d'extensions. Cette mesure préventive vise à limiter les risques d'attaques par "supply chain" (chaîne d'approvisionnement), en créant une fenêtre de protection permettant de détecter et de supprimer les versions malveillantes avant qu'elles ne soient massivement déployées chez les utilisateurs.

**Points clés :**
*   **Fonctionnement :** Les mises à jour automatiques sont différées de deux heures après leur publication.
*   **Flexibilité :** Les utilisateurs conservent la possibilité de forcer une mise à jour manuelle immédiate via l'interface.
*   **Exceptions :** Les extensions provenant d'éditeurs de confiance (Microsoft, GitHub, OpenAI) sont exemptées de ce délai et continuent d'être mises à jour instantanément.
*   **Tendance sectorielle :** Cette initiative s'inscrit dans une tendance globale de l'écosystème du développement (npm, pnpm, Yarn, Bun, RubyGems) visant à instaurer des délais de sécurité (« age gate ») pour contrer la propagation rapide de malwares dans les paquets logiciels.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais cible la vulnérabilité intrinsèque des chaînes d'approvisionnement logiciel où des versions corrompues ou malveillantes d'extensions légitimes sont publiées pour infecter les systèmes des développeurs.

**Recommandations :**
*   **Pour les utilisateurs :** Maintenez VS Code à jour vers la version 1.123 ou supérieure pour bénéficier de cette protection native.
*   **Gestion des mises à jour :** Soyez vigilant lors de l'installation immédiate d'extensions dont la mise à jour est en attente, particulièrement si elles ne proviennent pas d'éditeurs vérifiés.
*   **Adoption de bonnes pratiques :** Pour les environnements critiques, privilégiez l'utilisation d'extensions d'éditeurs reconnus et audités.

---
[Source](https://thehackernews.com/2026/06/vs-code-adds-2-hour-extension-auto.html){:target="_blank"}
