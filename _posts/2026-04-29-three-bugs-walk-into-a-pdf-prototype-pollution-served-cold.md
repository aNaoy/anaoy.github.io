---
title: 'Three Bugs Walk Into a PDF: Prototype Pollution, Served Cold'
date: 2026-04-29
permalink: /posts/2026/04/29/three-bugs-walk-into-a-pdf-prototype-pollution-served-cold/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse d'une chaîne d'exploitation Zero-Day dans Adobe Acrobat

En avril 2026, Adobe a publié des mises à jour d'urgence pour corriger trois vulnérabilités critiques dans Acrobat DC et Reader DC, exploitées activement « dans la nature » (ITW). Ces failles permettent à un attaquant de contourner les restrictions de sécurité, d'exécuter du code arbitraire et d'accéder à des fichiers sensibles via une chaîne d'attaques par pollution de prototype.

#### Points clés
*   **Mécanisme d'attaque :** La combinaison de trois primitives permet de transformer une exécution JavaScript standard en une exécution privilégiée.
*   **Chaînage :** 
    1. L'attaquant injecte du code JavaScript via des identifiants de boutons de dialogue malformés.
    2. La pollution du prototype `swConn` permet de détourner les objets de connexion internes vers des objets contrôlés par l'attaquant.
    3. L'abus d'une confusion d'objets dans les flux de travail « partagés » (trusted workflows) permet d'élever les privilèges du code injecté.
*   **Impact :** Élévation de privilèges permettant l'exécution de fonctions « trusted » (app.trustedFunction), lecture arbitraire de fichiers et exécution de code non autorisé sur le système hôte.

#### Vulnérabilités identifiées
*   **CVE-2026-34621 :** Pollution de prototype liée à l'utilisation non sécurisée d'un identifiant global (`swConn`) dans le processus `SilentDocCenterLogin`.
*   **CVE-2026-34622 & CVE-2026-34626 :** Vulnérabilités complémentaires de pollution de prototype et de confusion d'objets (notamment dans la gestion des chemins de documents `doc.path` et les alertes dynamiques `ANFancyAlertImpl`).

#### Recommandations
*   **Mise à jour immédiate :** Appliquer sans délai les correctifs fournis par Adobe via les bulletins de sécurité **APSB26-43** et **APSB26-44**. 
*   **Veille et patching :** S'assurer que les versions installées sont supérieures aux correctifs mentionnés (ex: versions postérieures à 26.001.21431).
*   **Défense en profondeur :** Bien que ces failles soient logicielles, la limitation des privilèges utilisateur sur les postes de travail et l'utilisation de solutions de sécurité capables de détecter des comportements anormaux (EDR) au niveau de l'exécution des processus Adobe sont recommandées pour limiter l'impact d'une exploitation réussie.

---
[Source](https://starlabs.sg/blog/2026/04-three-bugs-walk-into-a-pdf-prototype-pollution-served-cold/){:target="_blank"}
