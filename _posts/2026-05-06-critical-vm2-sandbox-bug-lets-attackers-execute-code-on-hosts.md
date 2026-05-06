---
title: 'Critical vm2 sandbox bug lets attackers execute code on hosts'
date: 2026-05-06
permalink: /posts/2026/05/06/critical-vm2-sandbox-bug-lets-attackers-execute-code-on-hosts/
tags:
- veille-cyber
- bleepingcomp
---
### Évasion critique de bac à sable dans la bibliothèque Node.js vm2

Une faille de sécurité critique a été découverte dans la bibliothèque de sandboxing `vm2`, largement utilisée pour exécuter du code JavaScript non fiable. Cette vulnérabilité permet à un attaquant de s'échapper de l'environnement isolé et d'exécuter des commandes arbitraires sur le système hôte.

**Points clés :**
*   **Fonctionnement de l'attaque :** La faille exploite la gestion des exceptions WebAssembly au sein du moteur V8. En manipulant des erreurs `TypeError` spécifiques via une conversion "Symbol-to-string", un attaquant peut faire fuiter des objets du contexte hôte vers le bac à sable.
*   **Impact :** Une fois l'objet hôte récupéré, l'attaquant peut exploiter la chaîne de constructeurs pour accéder à des API sensibles de Node.js (telles que `process` ou le système de fichiers).
*   **Contexte :** Le problème est spécifique aux environnements utilisant Node.js 25 avec la gestion des exceptions WebAssembly et le support JSTag activés.

**Vulnérabilités identifiées :**
*   **CVE-2026-26956 :** Vulnérabilité principale de sortie de bac à sable (sandbox escape).
*   *Note :* L'article mentionne également d'autres failles historiques sur la même bibliothèque, telles que CVE-2026-22709, CVE-2023-30547, CVE-2023-29017 et CVE-2022-36067.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **3.10.5** au minimum, la version la plus récente recommandée étant la **3.11.2**.
*   **Surveillance :** Étant donné l'historique de vulnérabilités critiques affectant `vm2`, il est conseillé aux développeurs d'évaluer la robustesse de leur stratégie d'isolation pour l'exécution de code tiers.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-vm2-sandbox-bug-lets-attackers-execute-code-on-hosts/){:target="_blank"}
