---
title: 'Hackers can bypass npm’s Shai-Hulud defenses via Git dependencies'
date: 2026-01-26
permalink: /posts/2026/01/26/hackers-can-bypass-npms-shai-hulud-defenses-via-git-dependencies/
tags:
- veille-cyber
- bleepingcomp
---
**Contournement des protections NPM via les dépendances Git**

Des vulnérabilités baptisées "PackageGate" ont été découvertes dans plusieurs gestionnaires de paquets JavaScript, y compris NPM. Ces failles permettent aux attaquants de contourner les mesures de sécurité conçues pour prévenir les attaques de la chaîne d'approvisionnement logicielle, notamment après les incidents "Shai-Hulud".

Les chercheurs de Koi Security ont identifié que lorsqu'NPM installe une dépendance depuis un dépôt Git, des fichiers de configuration malveillants peuvent détourner le chemin du binaire Git. Cela autorise l'exécution de code arbitraire, même lorsque l'option "--ignore-scripts" est activée. Cette technique a déjà été utilisée pour créer des shells inversés.

Pour d'autres gestionnaires comme pnpm et vlt, un contournement de l'intégrité du fichier de verrouillage est également possible.

**Points Clés :**

*   Les défenses de NPM, mises en place suite aux attaques "Shai-Hulud", peuvent être contournées.
*   Le vecteur d'attaque utilise les dépendances Git et des fichiers de configuration malveillants.
*   L'exécution de scripts peut être forcée même avec `--ignore-scripts`.
*   Des preuves d'utilisation de cette technique pour des attaques réelles existent.

**Vulnérabilités :**

*   Exécution de code à distance via des dépendances Git dans NPM.
*   Contournement de l'intégrité du fichier de verrouillage dans pnpm et vlt.
*   **CVEs mentionnées :** CVE-2025-69263 et CVE-2025-69264 pour pnpm.

**Recommandations :**

*   **Pour les utilisateurs de NPM :** Bien que NPM considère ce comportement comme attendu, la vigilance est de mise. Il est crucial de vérifier la fiabilité des paquets installés, particulièrement ceux provenant de dépôts Git. L'utilisation de l'authentification à deux facteurs et de jetons d'accès granulaires est encouragée.
*   **Pour les autres gestionnaires de paquets :** Des correctifs sont disponibles pour Bun (version 1.3.5), vlt et pnpm (incluant les CVE-2025-69263 et CVE-2025-69264). Il est recommandé de mettre à jour ces outils.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-can-bypass-npms-shai-hulud-defenses-via-git-dependencies/){:target="_blank"}
