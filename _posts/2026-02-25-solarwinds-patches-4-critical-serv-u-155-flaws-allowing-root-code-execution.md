---
title: 'SolarWinds Patches 4 Critical Serv-U 15.5 Flaws Allowing Root Code Execution'
date: 2026-02-25
permalink: /posts/2026/02/25/solarwinds-patches-4-critical-serv-u-155-flaws-allowing-root-code-execution/
tags:
- veille-cyber
- hackernews
---
### Correction de failles critiques dans SolarWinds Serv-U

SolarWinds a corrigé quatre vulnérabilités critiques dans son logiciel de transfert de fichiers Serv-U, version 15.5. Ces failles, toutes notées 9.1 sur l'échelle CVSS, permettent l'exécution de code à distance avec des privilèges root.

**Points clés :**

*   Quatre failles de sécurité critiques ont été corrigées dans SolarWinds Serv-U 15.5.
*   L'exploitation réussie de ces failles peut mener à l'exécution de code arbitraire à distance avec des privilèges root.
*   L'exploitation nécessite des privilèges administratifs.

**Vulnérabilités corrigées :**

*   **CVE-2025-40538** : Contrôle d'accès défaillant permettant à un attaquant de créer un utilisateur administrateur système et d'exécuter du code arbitraire en tant que root, via des privilèges d'administrateur de domaine ou de groupe.
*   **CVE-2025-40539** : Confusion de type permettant à un attaquant d'exécuter du code natif arbitraire en tant que root.
*   **CVE-2025-40540** : Confusion de type permettant à un attaquant d'exécuter du code natif arbitraire en tant que root.
*   **CVE-2025-40541** : Référence directe d'objet non sécurisée (IDOR) permettant à un attaquant d'exécuter du code natif en tant que root.

**Recommandations :**

*   Les utilisateurs de SolarWinds Serv-U doivent impérativement mettre à jour vers la version 15.5.4 pour bénéficier des correctifs.
*   Bien que l'exploitation nécessite des privilèges administratifs et que le risque soit considéré comme moyen sous Windows en raison de l'exécution par défaut sous des comptes moins privilégiés, la mise à jour reste une mesure essentielle.

---
[Source](https://thehackernews.com/2026/02/solarwinds-patches-4-critical-serv-u.html){:target="_blank"}
