---
title: 'Next.js Ships Out-of-Band Patch for Two Critical RCE Flaws in Caching and SVG Processing'
date: 2026-10-15
permalink: /posts/2026/10/15/nextjs-ships-out-of-band-patch-for-two-critical-rce-flaws-in-caching-and-svg-processing/
tags:
- veille-cyber
- hackernews
---
### Mise à jour de sécurité critique pour Next.js : Correction de vulnérabilités RCE et DoS

Next.js a publié un correctif d'urgence pour résoudre trois vulnérabilités majeures, dont deux failles d'exécution de code à distance (RCE) critiques notées 9.5 sur l'échelle CVSS.

#### Points clés
*   Les correctifs sont intégrés dans les versions **16.4.1** et **15.5.28**.
*   Les failles concernent le routage des composants serveur (React Server Components), le traitement des images SVG via la bibliothèque `sharp`, et les "Server Actions".
*   Les outils de scan de dépendances (comme `npm audit`) peuvent ne pas détecter ces vulnérabilités, car elles n'apparaissent pas encore dans tous les flux de sécurité.

#### Vulnérabilités identifiées
*   **RCE via `use cache` (GHSA-673q-mjm6-r5xr) :** Affecte les applications utilisant le *App Router* avec la mise en cache activée.
*   **RCE via le traitement SVG (CVE-2026-96889 / GHSA-2464-fhr4-w9xw) :** Exploitabilité liée à la bibliothèque `librsvg` utilisée par `sharp` sur les environnements Linux basés sur glibc.
*   **Déni de service (DoS) (GHSA-p3m5-59mp-jv5r) :** Affecte les applications avec des "Server Actions", permettant à un attaquant de saturer l'utilisation CPU du serveur.

#### Recommandations
1.  **Mise à jour immédiate :** Passer à la version **16.4.1** (ou **15.5.28** pour la branche 15).
2.  **Vérification de la dépendance `sharp` :** Pour la version 15.5.28, s'assurer manuellement que `sharp` est mis à jour vers la version **0.35.5 ou ultérieure** (`npm ls sharp`).
3.  **Contournement temporaire (Image) :** Si la mise à jour est impossible, désactiver le rendu SVG dans `sharp` ou bloquer le traitement des fichiers SVG via `sharp.block({ operation: ["VipsForeignLoadSvg"] })`.
4.  **Redéploiement :** Une fois les versions mises à jour, il est impératif de reconstruire et redéployer l'intégralité de l'application.

---
[Source](https://thehackernews.com/2026/10/nextjs-ships-out-of-band-patch-for-two.html){:target="_blank"}
