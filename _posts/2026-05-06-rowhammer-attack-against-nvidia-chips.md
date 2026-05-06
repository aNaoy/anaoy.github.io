---
title: 'Rowhammer Attack Against NVIDIA Chips'
date: 2026-05-06
permalink: /posts/2026/05/06/rowhammer-attack-against-nvidia-chips/
tags:
- veille-cyber
- schneier
---
### Vulnérabilités Rowhammer sur les GPU NVIDIA

Des chercheurs ont démontré de nouvelles méthodes d'attaque Rowhammer exploitant les puces graphiques NVIDIA de génération Ampere (notamment les modèles RTX 3060, RTX A6000 et RTX 6000). Ces failles permettent de corrompre la mémoire GDDR6 pour obtenir un accès arbitraire en lecture/écriture à la mémoire du CPU, menant à une compromission totale du système hôte et à l'obtention des privilèges root.

**Points clés :**
*   **Techniques d'attaque :** Les méthodes *GDDRHammer* et *GeForge* utilisent des schémas de martelage (hammering) spécifiques pour induire des basculements de bits (bitflips) dans les tables de pages du GPU.
*   **Impact :** Une fois la mémoire du GPU compromise, l'attaquant peut escalader ses privilèges pour prendre le contrôle total du système d'exploitation.
*   **Contournement de la sécurité :** Bien que l'attaque initiale nécessite la désactivation de l'IOMMU, une troisième variante de l'attaque a prouvé qu'il était possible d'obtenir un accès root même lorsque l'IOMMU est activé.

**Vulnérabilités :**
*   Pas de CVE spécifique mentionnée dans l'article, car les recherches portent sur des failles matérielles liées à l'architecture DRAM/GDDR.

**Recommandations :**
*   **Activation de l'IOMMU :** Maintenir l'IOMMU (Input-Output Memory Management Unit) activé dans les paramètres du BIOS/UEFI, car il constitue une barrière de sécurité essentielle, même si des chercheurs ont démontré qu'elle pouvait être contournée dans certains cas.
*   **Veille de sécurité :** Surveiller les publications des constructeurs concernant des mises à jour de firmware ou de microcode visant à atténuer les attaques Rowhammer au niveau des contrôleurs mémoire des GPU.
*   **Isolation :** Limiter l'exécution de codes non fiables ou de bibliothèques tierces sur des systèmes manipulant des données sensibles, compte tenu de la capacité des GPU à outrepasser les protections logicielles classiques.

---
[Source](https://www.schneier.com/blog/archives/2026/05/rowhammer-attack-against-nvidia-chips.html){:target="_blank"}
