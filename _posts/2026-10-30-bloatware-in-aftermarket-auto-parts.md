---
title: 'Bloatware in Aftermarket Auto Parts'
date: 2026-10-30
permalink: /posts/2026/10/30/bloatware-in-aftermarket-auto-parts/
tags:
- veille-cyber
- schneier
---
### Espionnage et vulnérabilités dans les systèmes multimédias automobiles

L'installation d'unités multimédias « aftermarket » bon marché provenant de plateformes comme Amazon présente des risques de sécurité majeurs. L'analyse assistée par intelligence artificielle d'un de ces appareils a révélé la présence massive de logiciels préinstallés malveillants agissant comme des logiciels espions.

**Points clés :**
*   **Comportement intrusif :** Utilisation intensive des ressources système (un tiers de la puissance de calcul même en veille) par un assistant vocal doté de fonctions *WebView*.
*   **Collecte de données :** Présence de services de géolocalisation (Baidu) et d'un enregistreur d'appels non sollicité.
*   **Accessibilité de l'analyse :** La facilité avec laquelle un utilisateur lambda peut désormais procéder à l'ingénierie inverse de firmwares complexes grâce à l'IA laisse présager une multiplication des découvertes de vulnérabilités IoT.

**Vulnérabilités :**
*   L'article n'identifie pas de CVE spécifique, mais souligne une architecture logicielle intrinsèquement non sécurisée, caractérisée par l'exécution de processus en arrière-plan non autorisés et une surface d'attaque étendue via des composants Android obsolètes ou mal configurés (*WebView*).

**Recommandations :**
*   Privilégier les équipements de marques reconnues dont la chaîne d'approvisionnement logicielle est transparente.
*   Se méfier des produits électroniques « sans nom » à bas prix, souvent livrés avec des firmwares contenant des logiciels superflus ou malveillants.
*   Être conscient que l'intégration de tels appareils dans un véhicule peut compromettre la confidentialité des données personnelles et potentiellement la sécurité du réseau interne du véhicule.

---
[Source](https://www.schneier.com/blog/archives/2026/10/bloatware-in-aftermarket-auto-parts.html){:target="_blank"}
