---
title: 'Next.js Patches Critical AVIF and Windows Flaws Enabling Unauthenticated RCE'
date: 2026-08-27
permalink: /posts/2026/08/27/nextjs-patches-critical-avif-and-windows-flaws-enabling-unauthenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Next.js : Exécution de code à distance (RCE)

Vercel a publié des correctifs de sécurité pour deux vulnérabilités critiques permettant l'exécution de code à distance (RCE) non authentifiée dans le framework Next.js.

**Points clés :**
*   **Impact :** Compromission totale possible du serveur.
*   **Versions affectées :** Next.js 13.4 à 15.5.23 et 16.0 à 16.3.2.
*   **Protection Vercel :** Les applications hébergées sur la plateforme Vercel sont protégées nativement et ne nécessitent aucune intervention.
*   **Contexte :** Ces correctifs font partie du programme mensuel de sécurité de Vercel, accéléré en raison de la gravité des failles découvertes.

**Vulnérabilités :**
1.  **CVE-2026-75604 (Score CVSS : 9.0) :** faille de *path traversal* (traversée de chemin) spécifique aux serveurs utilisant un système de fichiers Windows.
2.  **GHSA-2xp9-vwfh-vxw4 (Score CVSS : 9.5) :** débordement de tampon (*heap buffer overflow*) dans la bibliothèque `libheif` (via le package `sharp`), exploitable par le traitement d'images AVIF malveillantes.

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions **15.5.24** (Maintenance LTS) ou **16.3.3** (Active LTS) via `npm install next@15.5.24` ou `npm install next@16.3.3`.
*   **Atténuation AVIF :** Si la mise à jour n'est pas immédiatement possible, désactiver la prise en charge du format `image/avif` dans la configuration `next.config.js` pour limiter l'exposition à la faille `libheif`.
*   **Priorité Windows :** Il n'existe aucun contournement pour la faille Windows ; la mise à jour est impérative pour les déploiements auto-hébergés sur cet OS.

---
[Source](https://thehackernews.com/2026/08/nextjs-patches-critical-avif-and.html){:target="_blank"}
