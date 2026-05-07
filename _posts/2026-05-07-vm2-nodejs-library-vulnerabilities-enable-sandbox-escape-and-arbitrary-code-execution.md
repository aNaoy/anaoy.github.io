---
title: 'vm2 Node.js Library Vulnerabilities Enable Sandbox Escape and Arbitrary Code Execution'
date: 2026-05-07
permalink: /posts/2026/05/07/vm2-nodejs-library-vulnerabilities-enable-sandbox-escape-and-arbitrary-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques de la bibliothèque Node.js vm2 : Évasions de bac à sable

La bibliothèque open-source **vm2**, utilisée pour isoler et exécuter du code JavaScript non fiable, a été victime d'une série de douze vulnérabilités critiques. Ces failles permettent à un attaquant de contourner l'isolation du bac à sable (sandbox escape) et d'exécuter du code arbitraire sur le système hôte.

#### Points clés
*   **Nature des failles :** Les vulnérabilités exploitent divers mécanismes de JavaScript (objets, prototypes, gestion des erreurs) pour briser l'environnement sécurisé et accéder aux ressources du système hôte.
*   **Sévérité :** La majorité des failles présentent des scores CVSS proches ou égaux à 10.0, soulignant un risque extrême d'exécution de code à distance (RCE).
*   **Complexité de l'isolation :** Ces découvertes illustrent la difficulté persistante de sécuriser un bac à sable basé sur le moteur Node.js, malgré les mises à jour fréquentes du mainteneur.

#### Vulnérabilités (CVE)
Le tableau ci-dessous liste les vulnérabilités identifiées et leurs correctifs associés :

| CVE | Score CVSS | Correctif |
| :--- | :--- | :--- |
| **CVE-2026-24118** | 9.8 | v3.11.0 |
| **CVE-2026-24120** | 9.8 | v3.10.5 |
| **CVE-2026-24781** | 9.8 | v3.11.0 |
| **CVE-2026-26332** | 9.8 | v3.11.0 |
| **CVE-2026-26956** | 9.8 | v3.10.5 |
| **CVE-2026-43997** | 10.0 | v3.11.0 |
| **CVE-2026-43999** | 9.9 | v3.11.0 |
| **CVE-2026-44005** | 10.0 | v3.11.0 |
| **CVE-2026-44006** | 10.0 | v3.11.0 |
| **CVE-2026-44007** | 9.1 | v3.11.1 |
| **CVE-2026-44008** | 9.8 | v3.11.2 |
| **CVE-2026-44009** | 9.8 | v3.11.2 |

#### Recommandations
*   **Mise à jour immédiate :** Tous les utilisateurs de `vm2` doivent impérativement mettre à jour leur bibliothèque vers la **version 3.11.2** ou supérieure.
*   **Veille de sécurité :** Compte tenu de la fréquence élevée de découverte de failles de type "sandbox escape" dans `vm2`, il est conseillé aux organisations d'évaluer la pertinence de cette solution pour isoler du code hautement critique ou non fiable.

---
[Source](https://thehackernews.com/2026/05/vm2-nodejs-library-vulnerabilities.html){:target="_blank"}
