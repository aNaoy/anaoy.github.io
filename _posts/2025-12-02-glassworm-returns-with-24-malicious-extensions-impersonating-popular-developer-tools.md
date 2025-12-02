---
title: 'GlassWorm Returns with 24 Malicious Extensions Impersonating Popular Developer Tools'
date: 2025-12-02
permalink: /posts/2025/12/02/glassworm-returns-with-24-malicious-extensions-impersonating-popular-developer-tools/
tags:
- veille-cyber
- hackernews
---
**Le Retour de GlassWorm : 24 Extensions Malveillantes Usurpent des Outils de Développement Populaires**

La campagne de la chaîne d'approvisionnement connue sous le nom de GlassWorm refait surface, compromettant le Microsoft Visual Studio Marketplace et Open VSX avec 24 extensions qui se font passer pour des outils et frameworks de développement populaires tels que Flutter, React, Tailwind, Vim et Vue. Ces extensions manipulent les décomptes de téléchargements pour paraître légitimes et sont placées à proximité des projets authentiques afin de tromper les développeurs.

GlassWorm utilise la blockchain Solana pour ses communications de commande et de contrôle (C2), vole les identifiants des dépôts npm, Open VSX, GitHub et Git, draine des cryptomonnaies et transforme les machines des développeurs en nœuds contrôlés par les attaquants. Les identifiants volés sont cruciaux pour compromettre d'autres packages et extensions, permettant ainsi au malware de se propager comme un ver. Malgré les efforts de Microsoft et d'Open VSX, le malware a réapparu plusieurs fois, ciblant notamment les dépôts GitHub.

La nouvelle vague de la campagne intègre des implants basés sur Rust conditionnés dans les extensions. L'analyse d'une extension ("icon-theme-materiall") a révélé deux implants Rust, conçus pour cibler les systèmes Windows et macOS, capables de récupérer les détails du serveur C2 à partir d'une adresse de portefeuille Solana et de télécharger une charge utile chiffrée. En secours, ils peuvent analyser un événement Google Calendar pour trouver l'adresse C2.

**Points Clés:**

*   **Réapparition de GlassWorm :** La campagne de malware de la chaîne d'approvisionnement est de retour avec une nouvelle vague d'attaques.
*   **Usurpation d'Identité :** 24 extensions malveillantes se font passer pour des outils de développement populaires sur les marketplaces de Visual Studio et Open VSX.
*   **Ingénierie Sociale :** Gonflage artificiel des téléchargements et placement stratégique pour tromper les développeurs.
*   **Propagation par la Chaîne d'Approvisionnement :** Utilisation des identifiants volés pour compromettre d'autres extensions et propager le malware.
*   **Utilisation de la Blockchain et des Calendriers :** La blockchain Solana est utilisée pour le C2, avec Google Calendar comme mécanisme de secours.
*   **Implants Basés sur Rust :** Les nouvelles itérations intègrent des implants en Rust pour Windows et macOS.

**Vulnérabilités:**

*   Bien que l'article ne détaille pas de CVE spécifiques, la vulnérabilité réside dans la confiance accordée aux extensions sur les marketplaces et la capacité des attaquants à contourner les filtres de sécurité pour publier du code malveillant. Les extensions peuvent être approuvées initialement, puis mises à jour avec du code malveillant, souvent après leur activation.

**Recommandations:**

*   **Vigilance accrue des développeurs :** Examiner attentivement la source, la réputation et les autorisations des extensions avant de les installer.
*   **Vérification des auteurs et des téléchargements :** Être méfiant des extensions avec des noms similaires à des outils populaires ou des décomptes de téléchargements suspects.
*   **Maintien des systèmes à jour :** Appliquer régulièrement les mises à jour de sécurité pour les outils de développement et les systèmes d'exploitation.
*   **Suivi des annonces de sécurité :** Rester informé des nouvelles menaces et des vulnérabilités découvertes.
*   **Utilisation d'outils de sécurité :** Envisager des solutions de sécurité capables de détecter et de bloquer les menaces au niveau de la chaîne d'approvisionnement logicielle.

---
[Source](https://thehackernews.com/2025/12/glassworm-returns-with-24-malicious.html){:target="_blank"}
