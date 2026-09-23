---
title: 'Critical Next.js ImageResponse Flaw Can Lead to Server Code Execution via Crafted SVG Input'
date: 2026-09-23
permalink: /posts/2026/09/23/critical-nextjs-imageresponse-flaw-can-lead-to-server-code-execution-via-crafted-svg-input/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code dans Next.js via ImageResponse

Une faille de sécurité critique a été identifiée dans la fonctionnalité `ImageResponse` de Next.js. Elle permet à un attaquant d'exécuter du code arbitraire sur le serveur en injectant des entrées malveillantes dans les contenus SVG générés pour les prévisualisations d'images (Open Graph).

**Points clés :**
*   **Cause racine :** La bibliothèque `Satori` (utilisée par Next.js pour convertir le contenu en SVG) omet d'échapper correctement certaines entrées, permettant à des données contrôlées par l'utilisateur d'être interprétées comme du code SVG au lieu de simple texte.
*   **Vecteur d'attaque :** Les applications vulnérables sont celles qui intègrent directement des valeurs provenant de l'URL ou des requêtes utilisateur dans les attributs, styles ou contenus des SVG.
*   **Impact :** Exécution de code à distance (RCE) sur le serveur.
*   **Environnement :** La vulnérabilité concerne uniquement les applications utilisant le runtime Node.js. Le runtime Edge n'est pas affecté.

**Vulnérabilité :**
*   **CVE-2026-94545** (Score CVSS : 9.5)
*   **Versions affectées :** Next.js 16.2.0 à 16.3.5.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **Next.js 16.3.6**, qui inclut le correctif. Les utilisateurs des versions 15.5.x doivent migrer vers la version 15.5.26 pour bénéficier d'un renforcement de sécurité.
*   **Développement direct avec Satori :** Si vous utilisez `Satori` indépendamment de Next.js, mettez à jour vers la version **0.33.5**.
*   **Atténuation temporaire :** En cas d'impossibilité de mise à jour immédiate, assainissez strictement toutes les entrées utilisateur afin qu'elles ne soient jamais intégrées directement dans les attributs, styles ou contenus des éléments SVG.
*   **Audit :** Vérifiez tous les points de terminaison (`route handlers`) et les fichiers `opengraph-image` qui utilisent `next/og` pour identifier les entrées non sécurisées.

---
[Source](https://thehackernews.com/2026/09/critical-nextjs-imageresponse-flaw-can.html){:target="_blank"}
